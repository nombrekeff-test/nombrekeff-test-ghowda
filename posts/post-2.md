<!-- { "title": "My Second Blog", "labels": ["react", "code"] } -->

npm recently added **Unpacked Size** to the package details, I then realized one of my libraries was way too big (**350kb**) for the code it has...

I started looking into it, and realized a lot of files were being packaged and uploaded, even though they are ignored in `.gitignore`. 

The solution to this was to use [`.npmignore`](https://docs.npmjs.com/misc/developers#keeping-files-out-of-your-package) and ignore all the files you want to ignore, I knew about .npmignore but never thought of trying it out.

> As mentioned in the comments, this could also be accomplished using the [`files`](https://docs.npmjs.com/files/package.json#files) property in `package.json`.

I also used a tool called [`size-limit`](https://www.npmjs.com/package/size-limit) _that calculates the real cost to run your JS app or lib_, thanks to this I changed a couple of dependencies that were way too big for the use case, and reduced the size even more.
