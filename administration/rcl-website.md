# RCL Website

## Technology

The website was created in Hugo, a Go based static site generator. We used the Meghna theme and made some modifications for branding. 

The new RCL site is hosted on [Gitlab Pages](https://about.gitlab.com/product/pages/) in [this repo](https://gitlab.com/RiverCityLabs/website).  The repo is owned by the riveritylabs gmail account.

Gitlab Pages is a static site hosting service that is free for open source projects, which this website is.

Static sites have no backend database or services, which means the potential attack surface is vastly reduced which increases security immensely.

## Updating the Site

Any changes to the website must be made through that repo:

1. View the README.md for any considerations when updating the site
2. Create a [new branch](https://docs.gitlab.com/ee/gitlab-basics/create-branch.html#how-to-create-a-branch) based on the master branch
3. Make your changes
4. Submit a [Pull/Merge Request](https://docs.gitlab.com/ee/gitlab-basics/add-merge-request.html) to the master branch
5. One of the site admins will approve it and it will be merged
6. The site will auto build and publish the new changes

## DNS

DNS for gitlab proved obnoxious. [This thread](https://stackoverflow.com/questions/48913026/gitlab-pages-failed-to-verify-domain-ownership) helped.

![It required setting up two different domains in gitlab pages to have the site with with and without www.](../.gitbook/assets/image%20%2816%29.png)



For the current gitlab pages ip address, go [here](https://docs.gitlab.com/ee/user/gitlab_com/#gitlab-pages). Use this address for the `@` and `www` A-records

For the verification codes, you can get them from the gitlab project under Settings &gt; Pages &gt; click the domain you want the code for. There are different codes for `@` and `www`.

| Record Name | Record Type | Record Value |
| :--- | :--- | :--- |
| @ | A | 35.185.44.232 |
| www | A | 35.185.44.232 |
| @ | TXT | gitlab-pages-verification-code=aaabbbcccdddeeefffggg |
| www | TXT | gitlab-pages-verification-code=aaabbbcccdddeeefffggg |

