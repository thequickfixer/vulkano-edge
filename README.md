# Vulkano-edge

A Gentoo Vulkan Repository

# Information

Please check to see if your driver supports these new vulkan versions:

- Vulkan v1.3.210 has new extentions.
- Vulkan v1.3.211 has additional new extentions.

For ```vulkan-loader-9999``` ebuild from the gentoo overlay, check to see if the latest is working:

- [Vulkan-loader](https://github.com/KhronosGroup/Vulkan-Loader/actions?query=branch%3Amaster)

To unmask the ```vulkan-loader-9999``` ebuild, [this should help](https://wiki.gentoo.org/wiki/Knowledge_Base:Missing_keywords_and_keyword_requests)

# Repository Info

- Anything Vulkan related besides Vulkan-headers and Vulkan-loader will not be found here unless it's pushed.
- This repo will be always try to be updated to the latest, trying to have all versions for compatibility.

# How to install locally

Add this into /etc/portage/repos.conf/vulkano-edge.conf:

```
[vulkano-edge]
location = /var/db/repos/vulkano-edge
sync-type = git
sync-uri = https://github.com/thequickfixer/vulkano-edge.git
masters = gentoo
auto-sync = yes
```
Afterwards run:

```
sudo emaint sync --repo vulkano-edge
```
# How to install using layman

Update layman repos and add vulkano-edge as a repository:

```
sudo layman -f && sudo layman -a vulkano-edge
```
# How to emerge a version before v1.3.210

An example:

```
sudo emerge --ask =dev-util/vulkan-headers-1.3.209
```

For specifically this repo for whatever reason:

```
sudo emerge --ask =dev-util/vulkan-headers-1.3.209::vulkano-edge
```

# Notes

- Doing ```emerge --sync``` should update the repo when updating gentoo
- For using an older package, Gentoo likes to update the package to the latest unless specified in ```/etc/portage/..``` for more information visit [the gentoo wiki](https://wiki.gentoo.org) to try and mitigate Gentoo from updating the package to ```v1.3.210``` or later
