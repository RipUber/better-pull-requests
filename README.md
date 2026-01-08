# Do less reading on Gitlab's CI/CD
The idea here is to use large color blocks to identify important commits. I find highlighting prod releases handy so I can see what is in prod quickly. Depending on the project, it is also nice to highlight my commits or when staging branch has updated. You can do whatever you want! Add more colors if you want. You don't need to follow my lead either. If there is something you wish was better in gitlab or to fit your use case of gitlab and you control
![localImage](./images/readme.png)
## Change this extension to fit your needs

1. Open `custom-styles.css`
2. Now open a project CI/CD page in Gitlab. Open the inspector and do a search for `data-project` and the value of the data attribute is what you will use to scope your css to this projects CI/CD page.
3. In `custom-styles.css` change all instances of the following using your project name: `body[data-project="replace-me-with-your-project-name"]`.
4. For highlighting your commits or whatever you want to target find attributes with unique and consistent text. I leave my changes in the repo so you have an example of how it works.

## For Firefox based browsers

This can be tested by adding any file from the cloned directory in the `about:debugging` page `Load Temporary Add-on`. Though do note that doing this will not be permanent and will disappear if the browser is restarted.
1. Since this is a manifest v3 an ID will need to be provided. Add the following block to the manifest if it does not already exist

   ```yaml
    "browser_specific_settings": {
      "gecko": {
        "id": "jevan.meader@wheniwork.com"
      }
    }

2. Go to `about:config`
3. Search for `xpinstall.signatures.required` and set to `false`
4. Zip the folder `zip -rq better-gitlab.zip ./ -x "*.git/*"`
5. Go to extensions -> `Install Addon from file...`
# better-pull-requests
