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
