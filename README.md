# ThemeKit Tutorial

### Installation
- download the [ThemeKit .exe file](https://github.com/MikeC0xl0ng/ThemeKit-Tutorial/blob/8f88f54c3d18602cf276fe6ccd6c4eb706b8dbd4/theme.exe)
- put the file in the following path: C:\Program Files\Theme
- add a new environment variable 
  - we need it to be able to access theme.exe by typing `theme` and not `C:\Program Files\Theme\theme`
  - For Windows users: search for `environment variables`, then click `Add` and put the path of the theme.exe file, in our case is:
    >C:\Program Files\Theme

### Uses
---
#### Create your theme
- create a folder and navigate in it
- type `theme configure`  
  - the file tree gets created, you are ready to build your own theme!

##### Deploy it 
- type `theme new --password=private-app-password --store=storename.myshopify.com --name="name-of-the-theme"`
  - the password can be found in the private app  
  - with `--name` flag you specify name of the theme that will be shown in the Shopify dashboard
---  
#### Modify an existing theme
- create a folder and navigate in it
- create your config
  To do so you will need the following info:
  - password
    - the password of the private app with read and write `Theme` permission
  - theme_id
    - the id of the theme, you can find it by clicking `Edit code` of a theme https://shopName.myshopify.com/admin/themes/themeId
  - store
    - store url, make sure it is of the valid format => shopName.myshopify.com
- in the created file, paste the following snippet:
```
development:
  password: private-app-password
  theme_id: "themeId"
  store: shopName.myshopify.com
```
- open cmd
- type `theme download`
- when all the files are downloaded, type `theme watch` to update the theme gradually as you make changes
- open the theme in `preview` mode
- watch the changes in real time
  - the changes will be shown every time you modify and save a file 

###### Generic tips: 
1) make sure that in the store parameter you removed `/` sign from the end of the string 
   - shopName.myshopify.com instead of shopName.myshopify.com/
2) don't use `tab` during the creation of `config.yml` file: tab character is not accepted

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
