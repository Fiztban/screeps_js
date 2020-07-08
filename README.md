# Learning Screeps

> I have much to learn, but I know I don't know a lot, so I will start there.

I thought it was about time to learn to play this game that I have had on my to do list for a while. Here I will leave notes to myself that helped me with my learning.

***

## Setting Up Screeps

I went the route of using `VSCode` and `Github` which involved several things:

### Connecting Screeps to your Repo

Once you have created a Github account and created a repository for your screeps code and done a first commit  (usually a quick markdown file) you will want to link it to your screeps account:

1. Go to the [Screeps website](https://screeps.com/) and sign in as yourself. If you bought it via steam you will likely need to sign in that way.
2. Click your avatar in the top right corner and select `Manage Account`.
3. At the bottom you will find the `Github` section where you can link your screeps account to your repository. Click `Github user` to sign in, then click `Sync from repository` to select your newly made repository to connect to. Note you can choose to use a specific folder in that repository, but if you wish to use the root then leave the folder blank.

### Setting up VSCode

To use `VSCode` you will want to set up your files to work with your git repository, and have JavaScript auto-complete for the screeps game.

The following steps assume that you have already installed `VSCode`.

#### Linking VSCode to Git

There are several ways of doing this based on your current situation.

To work with `Git` you will need to have it installed on your computer already. If you don't you can find it [here](https://git-scm.com/downloads).

As mentioned above, these instructions assume you already have a `Github` account.

##### If You Have Made and Initialised a Repository And Have No Code Yet

I recommend doing it this way as it will involve less steps.

Because you should have already created your repository in Github, you will be wanting to `pull requesting` or `cloning` it to your local machine into the directory of your choice:

*You can also watch [this video](https://www.youtube.com/watch?v=sz2EM-gkEs0) of the process.*

1. Decide and create on your PC the directory that will contain your screeps code.
2. Check your settings have Git enabled checked by going to `File > Preferences > Settings (Ctrl+,)` then type `Git: enabled` and make sure that the option is checked.
3. On your Github page you will want to open the repository you created for screeps and click the `Clone or download` button and copy the URL, or simply copy the URL from your browser's address bar.
4. Go to the `Source Control` tab click on clone repository or go to your `Command Palette` with `View > Command Palette...` and type/select `Git: Clone`.
5. Within the `Command Palette` add your repository's URL.
6. You will be asked to select a folder, choose the directory you have made for your screeps code, or make create it at this point if you haven't already.

You will now have your repository (with only a readme file) `pulled` to that directory and opened in your `VSCode`.

##### If You Have Made and Initialised a Repository With Files And Have Code

This one takes a couple more steps, and is the way I went, so hopefully this helps others new to it like myself not have problems:

*You can also watch [this video](https://www.youtube.com/watch?v=3Tn58KQvWtU) of the process for the most part, it simply lacks the step of merging the repository content and your current code as they won't match.*

1. Open the screeps code directory in `VSCode` by going to `File > Open Folder` and then selecting the root folder for your code. This will open your files in the `Explorer` tab of `VSCode`. You can also do this by being in the `Explorer` tab and simply dragging and dropping the folder into the `Explorer` column.
2. Go to the `Source Control` tab and click `Initialise Repository` or go to your `Command Palette` with `View > Command Palette...` and type/select `Git: Initialize Repository`.
3. Select the folder from the `Command Palette` the correct folder name that matches your code's directory (that you added previously).
4. In the `Source Control` tab you will see that all your code files have a `U` next to them, this means they are `untracked` at this time. You will need to write a comment in the `Message` field and then click the check mark to `commit` it.
5. Add your `Github` repository by going back to your `Command Palette` and typing/selecting `Git: Add Remote`.
6. Within the `Command Palette` give it a name, its recommended to have the same name as your `Github` repo.
7. You will be asked to provide the URL of the repository within the `Command Palette`, you can obtain this by going to your Github page, opening your screeps repository click either clicking the `Clone or download` button to copy the URL, or simply copying the URL from your browser's address bar. paste this into the `Command Palette` and press enter.
8. Before you can `push` this `commit` however, you will need to `pull` your already initialised repository and this will require allowing the unrelated histories (of the `Github` repository and your directory) to come together. Open your `Terminal` by going to `View > Terminal (Ctrl+,)`.
9. First we will need to specify tracking information for your current `commit`, in the `Terminal` use the command:
 `git branch --set-upstream-to=<name of your Github repository>/master master`, just replace `<name of your Github repository>` with the actual name you gave your repo.
10. Next we will pull the unrelated histories together using the command `git pull --allow-unrelated-histories`.
11. Now we can `push` the `commit` by clicking the `...` button in `Source Control` and selecting `Push`.

Now your directory and `Github` repository will match and have all the files.

##### If You Have Code But Have Not Made a Repository

If you have already got code in you directory and have already initiated your Git repository then you can create a repository and connect it to your directory by simply doing:

*You can also watch [this video](https://www.youtube.com/watch?v=3Tn58KQvWtU) of the process.*

1. Open the screeps code directory in `VSCode` by going to `File > Open Folder` and then selecting the root folder for your code. This will open your files in the `Explorer` tab of `VSCode`. You can also do this by being in the `Explorer` tab and simply dragging and dropping the folder into the `Explorer` column.
2. Go to the `Source Control` tab and click `Initialize Repository` or go to your `Command Palette` with `View > Command Palette...` and type/select `Git: Initialize Repository`.
3. Select the folder from the `Command Palette` the correct folder name that matches your code's directory (that you added previously).
4. In the `Source Control` tab you will see that all your code files have a `U` next to them, this means they are `untracked` at this time. You will need to write a comment in the `Message` field and then click the check mark in the top right to `commit` it.
5. Go to your `Github` page to create your new screeps repository by clicking `New` on your repositories page.
6. Give it a `Name`, and choose whether it is public or private. Optionally add a description. Do NOT initialize the repository at this stage, if you do, follow from step 4 in the *If You Have Made and Initialised a Repository With Files And Have Code* section.
7. Click `Create Repository` and from the web page copy the URL showing in the `Quick setup` box, or just copy the URL from your browser's address bar.
8. Now add your `Github` repository to `VSCode` by going back to your `Command Palette` and typing/selecting `Git: Add Remote`.
9. Within the `Command Palette` give it a name, its recommended to have the same name as your `Github` repo.
10. Now paste the URL of your repository within the `Command Palette`.
11. You can now `push` your `commit` from the `Source Control` tab by pressing the `...` button and selecting `Push`.

You are now ready to send your code to Github, and this will then be added to your screeps.

#### Enabling Autocomplete for Screeps

The method I used was described in [this video](https://www.youtube.com/watch?v=GLwkTmjoyfM).

However, there is also [this set](https://github.com/daviddwlee84/Screeps) of instructions to install it using the [Garethp/ScreepsAutocomplete repo](https://github.com/Garethp/ScreepsAutocomplete).

I will detail the first method:

1. Install `Node.js` by downloading it from [this link](https://nodejs.org/en/download/).
2. Make sure that the `Add to PATH environment variable` is enabled during the install as this is required for the next steps to work.
3. Open the `Terminal` in `VSCode` by going to `View > Terminal (Ctrl+')`. NOTE: you may have to run `VSCode` in `Administrator mode` for this to work if you get error messages.
4. Type the command `npm` in the terminal to make sure `Node.js` has been added to PATH (you should see a list of helpful messages appear if it is installed). if it isn't you will have to go and add it to your PATH.
5. Type the following 2 commands
    * `npm install @types/screeps`
    * `npm install @types/lodash`

Once done you should be able to see [these API commands](https://docs.screeps.com/api/) suggest autocomplete options while typing your `JavaScript` code.