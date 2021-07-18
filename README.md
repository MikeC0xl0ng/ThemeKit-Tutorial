# ThemeKit Tutorial

### Installation
- download the [ThemeKit .exe file](https://github.com/MikeC0xl0ng/ThemeKit-Tutorial/blob/8f88f54c3d18602cf276fe6ccd6c4eb706b8dbd4/theme.exe)
- put the file in the following path: C:\Program Files\Theme
- add a new environment variable (we need it to be able to access theme.exe by digitin `theme` and not `C:\Program Files\Theme\theme`)
  - if you are running Windows => press `Win` and search for environment variables, then click `Add` and add the path of the theme.exe file, in our case is 
    >C:\Program Files\Theme

### Uses

##### Create your theme
- create a folder and navigate in it
- type `theme configure` => the file tree gets created, you are ready to build you own theme!

###### Deploy it 
- type `theme new --password=private-app-password --store=storename.myshopify.com --name="name-of-the-theme"`
-   with --name flag you specify name of the theme that will be shown in the Shopify dashboard
-   the password can be found in the private app

### Theme Architecture
Themes have a specific file structure, which contains the following directories:
- `Layout` 
- `Templates`
- `Sections`
- `Snippets`
- `Assets`
- `Config`
- `Locales`

Learn more about theme architecture [here](https://shopify.dev/themes/architecture#theme-directories).
