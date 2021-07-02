# Drupal9 - Content Staging/Propagation and Preview content using Deploy + Workspace + Replication + Multiversion + Relaxed
The Drupal Deploy module with the help of other Drupal modules allows users to easily stage and preview content for a Drupal site. It provides the capability to propagate content from one environment to another environment. There are various documents/forums available on the web to understand how these modules work in collaboration to implement this kind of solution. Here is the list of modules.

1. Deploy
2. Conflict
3. Workspace
4. Multiversion
5. Replication
6. Relaxed
7. Key Value


# Problem Statement
Recently I was upgrading a Drupal website to Drupal 9 and then I came across this architecture. Unfortunately, most of the modules were not ready for Drupal 9 and this whole setup was broken. I did try to find Drupal 9 patches for these but couldn't find them. One of the reasons is there is already a Workspaces module in Drupal core and hence it doesn't make sense to use contrib Workspace module. Though the Core module is not fully compatible with the above-listed modules.


# Solution
1. Use Core Workspaces module instead of Contrib workspace module. The plan was to use it along with other modules but it has a lot of compatibility issues with Deploy and other dependents modules. It seems so far it's not developed considering the Deploy solution in mind. Though it's still in experimental mode.
2. Since the Contrib workspace module is no longer available in D9 so was thinking to upgrade it to D9 to avoid any compatibility issues with other dependent modules. However, the Replication and Multiversion modules are not ready for D9 yet and they have a lot of deprecated code and other dependency issues.

I went ahead with #2 and start upgrading all the listed modules in D9.

Here's the list of patches for the corresponding modules.

| Module Name | Issue | D9 Patch | Comment |
| -------------| ------ | ------ | ------- |
| [Deploy](https://www.drupal.org/project/deploy) | https://www.drupal.org/project/deploy/issues/3221335 | https://www.drupal.org/files/issues/2021-06-29/Drupal9-Compatibility-Issues-3221335-2.patch | |
| [Workspace](https://www.drupal.org/project/workspace) | https://www.drupal.org/project/workspace/issues/3221374 | https://www.drupal.org/files/issues/2021-06-29/Drupal-9-compatibility-issues-3221374-1.patch | |
| [Multiversion](https://www.drupal.org/project/multiversion) | https://www.drupal.org/project/multiversion/issues/3221332 | https://www.drupal.org/files/issues/2021-06-29/Drupal-9-compatibility-issues-3221332-6.patch | |
| [Replication](https://www.drupal.org/project/replication) | https://www.drupal.org/project/replication/issues/3221333 | https://www.drupal.org/files/issues/2021-06-29/Drupal-9-compatibility-issues-3221333-5.patch | |
| [RELAXed Web Services](https://www.drupal.org/project/relaxed) | https://www.drupal.org/project/relaxed/issues/3221380 | https://www.drupal.org/files/issues/2021-06-29/Drupal-9-compatibility-issues-3221380-2.patch | |
