# RCL Website

## Technology

The website was created in Hugo, a Go based static site generator. We used the Meghna theme and made some modifications for branding. 

The new RCL site is hosted on [Gitlab Pages](https://about.gitlab.com/product/pages/) in [this repo](https://gitlab.com/RiverCityLabs/website).  The repo is owned by the riveritylabs gmail account.

Github pages is a static site hosting service that is free for open source projects.

Static sites have no backend database or services, which means the potential attack surface is vastly reduced which increases security immensely.

## Updating the Site

Any changes to the website must be made through that repo:

1. View the README.md for any considerations when updating the site
2. Create a [new branch](https://docs.gitlab.com/ee/gitlab-basics/create-branch.html#how-to-create-a-branch) based on the master branch
3.  make your changes
4. Submit a [Pull/Merge Request](https://docs.gitlab.com/ee/gitlab-basics/add-merge-request.html) to the master branch
5. One of the site admins will approve it and it will be merged
6. The site will auto build and publish the new changes

