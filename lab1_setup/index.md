---
layout: default
title: Lab 1 - Environment Setup
nav_order: 1
---

# Lab 1: Environment Setup

## Introduction
In this lab, we will focus on configuring our environment using an IDE and the Checkmarx plugin. For these labs we will be leveraging __Microsoft Visual Studio Code__ or __Cursor__, as they are free and commonly used. Checkmarx has integrated plugins with the following IDEs:

* IntelliJ
* Visual Studio
* VS Code
* Cursor

To learn more, checkout [Checkmarx Integrations with Popular IDEs](https://checkmarx.com/why-checkmarx/integrations/checkmarx-integrations-with-ides/) and [Checkmarx IDE Integration Documentation](https://docs.checkmarx.com/en/34965-68727-checkmarx-one-ide-plugins.html)

{: .warning }
For these labs, we are using a known vulnerable projects to demonstrate vulnerability detection and remediation capabilities.  Note that if this application is run, these applications can result in system crashes as a result of memory leaks, deadlock, JVM crashes, etc.  In these labs, we are only using Checkmarx solutions that scan source code, thus there is no reason or need to run this project and __it is not recommended to do so__. If you do wish to run the project, do so at your own risk. It is HIGHLY recommended you do so in a sandbox environment (e.g. within a VM).

## Install Your IDE
You can use either VS Code or Cursor for these labs. Choose one of the following:

### Option 1: VS Code
{: .note }
If you already have VS Code installed, you can skip this section. When we are done with the lab, you can always uninstall/disable the Checkmarx plugin

1. Navigate to [https://code.visualstudio.com/download](https://code.visualstudio.com/download) to download the Visual Studio Code installer for your operating system.
2. Install VS Code on your machine

### Option 2: Cursor
{: .note }
Cursor is an AI-powered code editor built on VS Code. If you already have Cursor installed, you can skip this section.

1. Navigate to [https://cursor.com/](https://cursor.com/) to download the Cursor installer for your operating system.
2. Install Cursor on your machine


## Install the Checkmarx Plugin

<div class="auth-tabs">
  <input type="radio" id="vscode-install-tab" name="install-method" checked>
  <label for="vscode-install-tab">VS Code</label>
  
  <input type="radio" id="cursor-install-tab" name="install-method">
  <label for="cursor-install-tab">Cursor</label>
  
  <div class="auth-content vscode-install-content" markdown="1">

### Installing in VS Code

The Visual Studio Code Extension is available on the [Visual Studio Code marketplace](https://marketplace.visualstudio.com/items?itemName=checkmarx.ast-results).

1. **Open VS Code** - Launch Visual Studio Code from your applications or desktop

2. **Access Extensions** - Click the Extensions icon in the left sidebar (or press `Ctrl+Shift+X` / `Cmd+Shift+X`)

    ![VS Code Extensions View](./assets/images/vscode_extensions_view.png "VS Code Extensions Panel")

3. **Search for Checkmarx** - In the search bar, type "Checkmarx" and press Enter

    ![Search Checkmarx](./assets/images/vscode_search_checkmarx.png "Search for Checkmarx")

4. **Install the Plugin** - Find "Checkmarx One" in the results and click the **Install** button

    ![Install Checkmarx Plugin](./assets/images/vscode_extensions.png "Checkmarx VS Code Plugin")

    {: .warning }
    **Important**: Ensure you select the plugin entitled "**Checkmarx One**" not "Checkmarx SAST x.x" (legacy version)

5. **Verify Installation** - After installation, the Checkmarx icon appears in the left-side navigation panel

    ![Checkmarx Plugin Installed](./assets/images/cx_plugin_installed.png "Checkmarx Plugin Installed")

6. **Plugin Ready** - You should now see the Checkmarx panel in your sidebar, ready for configuration

  </div>

  <div class="auth-content cursor-install-content" markdown="1">

### Installing in Cursor

Since Cursor is built on VS Code, it supports all VS Code extensions including the Checkmarx plugin.

1. **Open Cursor** - Launch Cursor from your applications or desktop

2. **Access Extensions** - Click the Extensions icon in the left sidebar (or press `Ctrl+Shift+X` / `Cmd+Shift+X`)

    ![Cursor Extensions View](./assets/images/cursor_extensions_view.png "Cursor Extensions Panel")

3. **Search for Checkmarx** - In the search bar, type "Checkmarx" and press Enter

    ![Cursor Search Checkmarx](./assets/images/cursor_search_checkmarx.png "Search for Checkmarx in Cursor")

4. **Install the Plugin** - Find "Checkmarx One" in the results and click the **Install** button

    ![Install Cursor Checkmarx Plugin](./assets/images/cursor_install_checkmarx.png "Checkmarx Cursor Plugin")

    {: .warning }
    **Important**: Ensure you select the plugin entitled "**Checkmarx One**" not "Checkmarx SAST x.x" (legacy version)

5. **Verify Installation** - After installation, the Checkmarx icon appears in the left-side navigation panel

    ![Cursor Checkmarx Plugin Installed](./assets/images/cursor_cx_plugin_installed.png "Cursor Checkmarx Plugin Installed")

6. **Plugin Ready** - You should now see the Checkmarx panel in your sidebar, ready for configuration

  </div>

</div>


## Configure the Checkmarx Plugin

<div class="auth-tabs">
  <input type="radio" id="vscode-config-tab" name="config-method" checked>
  <label for="vscode-config-tab">VS Code</label>
  
  <input type="radio" id="cursor-config-tab" name="config-method">
  <label for="cursor-config-tab">Cursor</label>
  
  <div class="auth-content vscode-config-content" markdown="1">

1. In VS Code, click on the Checkmarx extension icon and then click on the Open settings button.  
   The Checkmarx Settings form opens.  
   ![Configure Checkmarx Plugin](./assets/images/cx_plugin_config.png "Configure Checkmarx Plugin")

  </div>

  <div class="auth-content cursor-config-content" markdown="1">

1. In Cursor, click on the Checkmarx extension icon and then click on the Open settings button.  
   The Checkmarx Settings form opens.  
   ![Configure Cursor Checkmarx Plugin](./assets/images/cursor_cx_plugin_config.png "Configure Cursor Checkmarx Plugin")

  </div>

</div>

2. First you will need to authenticate the plugin by clicking the __Authentication__ link in box 1.  
   Once you click that, choose your method below to see the corresponding settings:

   {: .note }
   The preference for this workshop would be to use the Oauth authentication method. 


   <style>
   .auth-tabs {
     margin: 20px 0;
   }
   .auth-tabs input[type="radio"] {
     display: none;
   }
   .auth-tabs label {
     display: inline-block;
     padding: 10px 20px;
     background: #f0f0f0;
     border: 1px solid #ddd;
     cursor: pointer;
     margin-right: 5px;
   }
   .auth-tabs label:hover {
     background: #e0e0e0;
   }
   .auth-tabs input[type="radio"]:checked + label {
     background: #007acc;
     color: white;
   }
   .auth-content {
     display: none;
     padding: 20px;
     border: 1px solid #ddd;
     margin-top: 10px;
     clear: both;
   }
   .auth-tabs #oauth-tab:checked ~ .oauth-content,
   .auth-tabs #apikey-tab:checked ~ .apikey-content,
   .auth-tabs #asca-available-tab:checked ~ .asca-available-content,
   .auth-tabs #asca-unavailable-tab:checked ~ .asca-unavailable-content,
   .auth-tabs #vscode-install-tab:checked ~ .vscode-install-content,
   .auth-tabs #cursor-install-tab:checked ~ .cursor-install-content,
   .auth-tabs #vscode-config-tab:checked ~ .vscode-config-content,
   .auth-tabs #cursor-config-tab:checked ~ .cursor-config-content,
   .auth-tabs #vscode-connect-tab:checked ~ .vscode-connect-content,
   .auth-tabs #cursor-connect-tab:checked ~ .cursor-connect-content {
     display: block;
   }
   </style>

   <div class="auth-tabs">
     <input type="radio" id="oauth-tab" name="auth-method" checked>
     <label for="oauth-tab">OAuth Authentication</label>
     
     <input type="radio" id="apikey-tab" name="auth-method">
     <label for="apikey-tab">API Key Authentication</label>
     
     <div class="auth-content oauth-content">
       <img src="./assets/images/plugin_oauth_option.png" alt="OAuth Authentication" width="600">
       <p>
         The base URL for this lab will be: <code>https://us.ast.checkmarx.net</code>.<br>
         The Tenant Name will be delivered in the lab.
       </p>
     </div>

     <div class="auth-content apikey-content">
       <img src="./assets/images/plugin_api_auth_option.png" alt="API Key Authentication" width="600">
       <p>
         To use the API Key option, the instructions can be found at 
         <a href="https://docs.checkmarx.com/en/34965-188712-creating-api-keys.html" target="_blank">Generating a Checkmarx API Key</a>.
       </p>
     </div>
   </div>

  

3. Now that you have authenticated, in the Checkmarx AST plugin section, enter the following details:


    |         Item                          |          Value                |
    |:----------------------                |:-----------------------       |
    | Checkmarx One: Additional Params | \<leave blank\>                 |
    | Checkmarx KICS: Activate KICS Real-time Scanning | \<leave blank\>                 |
    | Checkmarx KICS: Additional Parameters | \<leave blank\> 

4. __Configure ASCA (AI Secure Coding Assistant)__: Choose your configuration based on availability:

   <div class="auth-tabs">
     <input type="radio" id="asca-available-tab" name="asca-config" checked>
     <label for="asca-available-tab">ASCA Available</label>
     
     <input type="radio" id="asca-unavailable-tab" name="asca-config">
     <label for="asca-unavailable-tab">ASCA Not Available</label>
     
     <div class="auth-content asca-available-content">
       <table>
         <tr>
           <th>Item</th>
           <th>Value</th>
         </tr>
         <tr>
           <td>Checkmarx AI Secure Coding Assistant (ASCA): Activate ASCA</td>
           <td><strong>Enable</strong></td>
         </tr>
         <tr>
           <td>Checkmarx Security Champion: Model</td>
           <td><strong>Optional:</strong> Choose a supported model</td>
         </tr>
         <tr>
           <td>Checkmarx Security Champion: Key</td>
           <td><strong>Optional:</strong> Utilize a GPT API-KEY from your organization</td>
         </tr>
       </table>
       <p><strong>Note:</strong> With ASCA enabled, you'll get real-time security feedback as you code in Lab 2.</p>
     </div>

     <div class="auth-content asca-unavailable-content">
       <table>
         <tr>
           <th>Item</th>
           <th>Value</th>
         </tr>
         <tr>
           <td>Checkmarx AI Secure Coding Assistant (ASCA): Activate ASCA</td>
           <td><strong>Leave Disabled</strong></td>
         </tr>
         <tr>
           <td>Checkmarx Security Champion: Model</td>
           <td><strong>Leave blank</strong></td>
         </tr>
         <tr>
           <td>Checkmarx Security Champion: Key</td>
           <td><strong>Leave blank</strong></td>
         </tr>
       </table>
       <p><strong>Note:</strong> You'll still be able to complete all labs. Some ASCA-specific features in Lab 2 will be unavailable.</p>
     </div>
   </div>

    {: .note }
    The AI Features may be disabled for your specific workshop due to organizational policy or licensing restrictions. 

5. Once entered, you have configured the plugin

6. Close the Plugin Settings Screen

## Connect to a project

<div class="auth-tabs">
  <input type="radio" id="vscode-connect-tab" name="connect-method" checked>
  <label for="vscode-connect-tab">VS Code</label>
  
  <input type="radio" id="cursor-connect-tab" name="connect-method">
  <label for="cursor-connect-tab">Cursor</label>
  
  <div class="auth-content vscode-connect-content" markdown="1">

1. Mouse-over the __Project:__ field in the left pane, click the pencil icon, then select the project name __TotallySecure__ that appears in the middle search bar

    ![Select Project](./assets/images/cx_select_project.png "Select the Project")

    {: .note }
    > Since Checkmarx plugin v2.34.0 release, only the AST/One API Key or OAuth is required to connect the plugin to a Checkmarx One tenant.  If you see a 404 error within VS Code when attempting to connect to a project while using the API Key option, it may be because environment variables are overriding the Uri/tenant names from the API key (cx_base_auth_uri, cx_base_uri, cx_tenant).  These variables are set if you've ever connected to Checkmarx One via the CLI. This can be fixed by deleting the checkmarxcli.yaml file if it exists on your machine.
    >
    > For Mac OSX and Linux, this file can be found at ~/.checkmarx/checkmarxcli.yaml
    >
    > For Windows, this file can be found at %UserProfile%\\.checkmarx\\checkmarxcli.yaml

2. Mouse-over the __Branch:__ field in the left pane, click the pencil icon, then select the branch __master__ that appears in the middle search bar

    ![Select Branch](./assets/images/cx_select_branch.png "Select a branch")

3. The Checkmarx Plugin is now configured and you should see scan results appear in the left pane

    ![Configuration Finished](./assets/images/cx_scan_results.png)

  </div>

  <div class="auth-content cursor-connect-content" markdown="1">

1. Mouse-over the __Project:__ field in the left pane, click the pencil icon, then select the project name __TotallySecure__ that appears in the middle search bar

    ![Cursor Select Project](./assets/images/cursor_cx_select_project.png "Select the Project in Cursor")

    {: .note }
    > Since Checkmarx plugin v2.34.0 release, only the AST/One API Key or OAuth is required to connect the plugin to a Checkmarx One tenant.  If you see a 404 error within Cursor when attempting to connect to a project while using the API Key option, it may be because environment variables are overriding the Uri/tenant names from the API key (cx_base_auth_uri, cx_base_uri, cx_tenant).  These variables are set if you've ever connected to Checkmarx One via the CLI. This can be fixed by deleting the checkmarxcli.yaml file if it exists on your machine.
    >
    > For Mac OSX and Linux, this file can be found at ~/.checkmarx/checkmarxcli.yaml
    >
    > For Windows, this file can be found at %UserProfile%\\.checkmarx\\checkmarxcli.yaml

2. Mouse-over the __Branch:__ field in the left pane, click the pencil icon, then select the branch __master__ that appears in the middle search bar

    ![Cursor Select Branch](./assets/images/cursor_cx_select_branch.png "Select a branch in Cursor")

3. The Checkmarx Plugin is now configured and you should see scan results appear in the left pane

    ![Cursor Configuration Finished](./assets/images/cursor_cx_scan_results.png)

  </div>

</div>


## Clone the project to your local machine

1. Open a terminal or command prompt and navigate to a directory or folder you'll be able to easily find (e.g. ~/ on Mac OSX and Linux or %UserProfile%/ on Windows)


2. Clone our example scanned project to your local machine.

        git clone https://github.com/HsecCx/workshop-TotallySecure.git

    {: .note }
    You will need __git__ installed on your local machine if it is not already installed. You can use [this guide ](https://github.com/git-guides/install-git) to see the steps for your operating system

3. Within your IDE (VS Code or Cursor), select __File__ > __Open Folder__, and select the directory __workshop-TotallySecure__.

4.  You may be prompted by your IDE asking if you trust the developers. We will not be executing any of this projects code and will just be reviewing the source, so you can safely accept. Once you complete the labs, you can safely delete the project.

    ![VS Code Trust Project](./assets/images/vscode_trust.png "IDE Trust Project")'


## Key Takeaways
- Checkmarx has IDE plugins for all major IDEs including VS Code and Cursor
- The Checkmarx One extension is available for both VS Code and Cursor and is distinct from the legacy Checkmarx SAST plugin
- The Checkmarx One extension can be connected to a Checkmarx One instance by configuring authentication (API Key or OAuth)
- Checkmarx scan results can be reviewed directly within your chosen IDE
- Both VS Code and Cursor provide the same Checkmarx functionality and user experience
- Docker is required for IaC/KICS autoremediation within both IDEs

