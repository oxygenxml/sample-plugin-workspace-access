# sample-plugin-workspace-access
Sample Maven-based workspace access plugin.

This sample plugin implements the plugin extension API: 

            ro.sync.exml.plugin.workspace.WorkspaceAccessPluginExtension

which allows you to add new toolbar, menu and contextual menu buttons, custom views and to interract with the opened XML documents.

For more details see: http://www.oxygenxml.com/doc/ug-editor/index.html#topics/workspace-access-plugin.html

If you are using the Eclipse workbench you can clone the project locally and use in the Eclipse the "Import->Existing Maven Projects" functionality.

Afterwards you can run "mvn install" (either from the command line or from the IDE as Eclipse already has Maven integrated: pom.xml-> Run as-> Maven install) to create a JAR containing the plugin folder in the project's "target" folder. 

In the same "target" folder there will be an "addon.xml" file allowing you to install the plugin directly from Oxygen (Help menu->Install new add-ons). Or you can manually unpack the JAR in the "OXYGEN_INSTALL_DIR/plugins" folder.

If you want to debug your Java code and do not want to run "mvn install" and to install the plugin in Oxygen all the time, in the "OXYGEN_INSTALL_DIR\plugins" folder you can create a folder with any name (for example "sample") in which you place a file called "plugin.redirect" containing the full file path reference to your project (for example in my case **C:\Users\radu_coravu\Documents\sample-plugin-workspace-access**). Make sure the order of elements in **runtime** from "plugin.xml" is as follows:

    <runtime>
        <library name="target/classes" />
	    <librariesFolder name="target/lib" />
	    <librariesFolder name="lib" />
    </runtime>
 
After this, when Oxygen will start, it will automatically load the plugin from your project location. So you will just need to modify the Java code, the IDE will automatically compile it, then restart Oxygen and test your changes.

Please keep in mind that if you have installed the add-ons first, you need to remove them from Oxygen if you want to make the current plugin work using the second solution with automatic loading.

Copyright and License
---------------------
Copyright 2018 Syncro Soft SRL.

This project is licensed under [Apache License 2.0](https://github.com/oxygenxml/sample-plugin-workspace-access/blob/master/LICENSE)
