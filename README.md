# sample-plugin-workspace-access
Sample Maven-based workspace access plugin.

This sample plugin implements the plugin extension API: 

            ro.sync.exml.plugin.workspace.WorkspaceAccessPluginExtension

For more details see: http://www.oxygenxml.com/doc/ug-editor/index.html#concepts/workspace-access-plugin.html

If you are using the Eclipse workbench you can clone the project locally and use in the Eclipse the "Import->Existing Maven Projects" functionality.

Afterwards you can run "mvn install" (either from the command line or from the IDE) to create a JAR containing the plugin folder in the project's "target" folder. 

In the same "target" folder there will be an "addon.xml" file allowing you to install the plugin directly from Oxygen (Help menu->Install new add-ons). Or you can manually unpack the JAR in the "OXYGEN_INSTALL_DIR/plugins" folder.


