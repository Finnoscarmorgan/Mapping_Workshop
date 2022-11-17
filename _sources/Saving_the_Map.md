# ...More on Sharing and Embedding Maps

You can share and embed your Kepler map by uploading your json file to [Gist Github](https://gist.github.com) (a repository for saving and sharing snippets of code) and then creating a custom URL to load this file into Kepler.gl. If you wish to embed your map on your own website you can wrap this URL in an iframe using an [i-frame generator](https://www.iframe-generator.com)

`````{admonition} Register for a Github Account
:class: tip
To share and embed your map you will need to register for an account with Github.

`````

## 1. Steps to Share your Map
1. Register for an account with [Github](https://github.com)
2. Download your map from Kepler.gl as a .json file.
3. Upload your .json file at [Github Gist](https://gist.github.com), you can copy and paste your code directly into the text-box.
4. Label your document with the extension '.json' 
5. Save the document by clicking the green button "Create Public Gist"
6. Click on the 'Raw' button, and copy the URL. It should look something like:
*"https://gist.githubusercontent.com/Githubusername/288fcad69348b8d88d2c78658e21b4e9/raw/298360c54a51c1490c3167aac7f3793bf42db34f/filename.json"*
7. You can use this URL, to load your map, its data and the map configurations directly into Kepler. Simply add the the URL above to the URL *"https://kepler.gl/#/demo?mapUrl="* 
Your final URL should look something like: 
*https://kepler.gl/#/demo?mapUrl=https://gist.githubusercontent.com/Githubusername/288fcad69348b8d88d2c78658e21b4e9/raw/298360c54a51c1490c3167aac7f3793bf42db34f/filename.json"*

## 2. Steps to Embed your Map
1. Using [iframe-generator.com](https://www.iframe-generator.com) you can add the URL you generated above to generate an iframe that can be directly embedded into a website. 