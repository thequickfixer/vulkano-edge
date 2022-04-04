# Vulkano-edge

A Gentoo Vulkan Repository

# Information

- Vulkan v1.3.210 has new extentions. To run those extentions check to see if your driver supports it.

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
sudo layman -f
sudo layman -a vulkano-edge
```

# Notes

- Doing a ```emerge --sync``` should update the repo when updating gentoo
