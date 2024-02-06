<div align='center'>


# HOW TO RUN

**Note: The below setup is very convoluted as this was done as a proof of concept, but capturing this for auditability**

### Setting up AWS toolkit locally

Steps:
1. Clone [aws-toolkit-vscode](https://github.com/aws/aws-toolkit-vscode) from Github
2. [TEMPORARY] Change to commit `819e63` as this has the `generateClients` script that is needed
3. Run `npm install`
4. Run `npm run generateClients`
5. Modify `featureDev.ts` to log on console the bearer token used (for local runs only, do NOT store this)
6. Run the VS code extension and trigger the codewhisperer client by starting Amazon Q chat
7. Retrieve bearer token from developer tools console

### Setting up Cat-GPT
1. Edit `callCodeWhispererClient()` in `basepettype.ts` to use the bearer token retrieved above
2. Copy the codewhisperer client to this package via `cp -r <PATH_TO_TOOLKIT>/aws-toolkit-vscode/src.gen/@amzn ./node_modules/`
3. Run `npm install <PATH_TO_TOOLKIT>/aws-toolkit-vscode/src.gen/@amzn/codewhisperer-streaming --save --no-audit`
4. Run `npm run compile`
5. Run the VS code extension and open developer tools console
6. Try hovering over the pets - this should call codewhisperer streaming client and have them say something!


# VS Code Pets

![icon](https://github.com/tonybaloney/vscode-pets/raw/master/icon.png)
</div>    

<p align="center">
    Puts a small, bored cat, an enthusiastic dog, a feisty snake, a rubber duck, or Clippy 📎 in your code editor to boost productivity.
    <br>
    <br>
    <a href="https://github.com/tonybaloney/vscode-pets/issues/new?assignees=&labels=feature&template=bug_report.md&title=">Report a Bug</a>
    ·
    <a href="https://github.com/tonybaloney/vscode-pets/issues/new?assignees=&labels=feature&template=feature_request.md&title=">Request feature</a>
</p>

[![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/tonybaloney.vscode-pets?color=blue&logo=visual-studio)](https://marketplace.visualstudio.com/items?itemName=tonybaloney.vscode-pets&WT.mc_id=python-17801-anthonyshaw)
[![Visual Studio Marketplace Installs](https://img.shields.io/visual-studio-marketplace/i/tonybaloney.vscode-pets?logo=visualstudio)](https://marketplace.visualstudio.com/items?itemName=tonybaloney.vscode-pets&WT.mc_id=python-17801-anthonyshaw)
[![Visual Studio Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/tonybaloney.vscode-pets?logo=visualstudio)](https://marketplace.visualstudio.com/items?itemName=tonybaloney.vscode-pets&WT.mc_id=python-17801-anthonyshaw)

![screenshot](https://github.com/tonybaloney/vscode-pets/raw/master/docs/source/_static/screenshot.gif)

## Installation

Install this extension from the [VS Code marketplace](https://marketplace.visualstudio.com/items?itemName=tonybaloney.vscode-pets&WT.mc_id=python-17801-anthonyshaw).

OR

With VS Code open, search for `vscode-pets` in the extension panel (`Ctrl+Shift+X` on Windows/Linux or `Cmd(⌘)+Shift+X` on MacOS) and click install.

OR

With VS Code open, launch VS Code Quick Open (`Ctrl+P` on Windows/Linux or `Cmd(⌘)+P` on MacOS), paste the following command, and press enter.

`ext install tonybaloney.vscode-pets`

## Using VS Code Pets

Congrats on installing joy! Enjoy interacting with these cute pixelated pets. Read below to get a full understanding of this extension. Not convinced? Watch our extension spotlight on [Visual Studio Code](https://www.youtube.com/watch?v=aE6Ifj_KstI).

After installing, open the command palette with `Ctrl+Shift+P` on Windows/Linux or `Cmd(⌘)+Shift+P` on MacOS.  

Run the "Start pet coding session" command (`vscode-pets.start`) to see a cat in VS Code:

![Default view](https://github.com/tonybaloney/vscode-pets/raw/master/docs/source/_static/pet-in-default-explorer.png)

[Now checkout the documentation to see what else is possible!](https://tonybaloney.github.io/vscode-pets)

## Translation

Visit the [Crowdin Project](https://crowdin.com/project/vscode-pets) in case you'd like to help with the translations. It will be synced automatically to the repository. You can also request a new language in the [Discussions](https://crowdin.com/project/vscode-pets/discussions) section.

## Credits

The cat animations were designed by [seethingswarm](https://seethingswarm.itch.io/catset). The dog media assets for this extension were designed by [NVPH Studio](https://nvph-studio.itch.io/dog-animation-4-different-dogs). 

The forest theme was designed by [edermunizz](https://edermunizz.itch.io/free-pixel-art-forest). The castle assets were created using artwork by [GuttyKreum](https://guttykreum.itch.io/gothic-castle-game-assets).

[Marc Duiker](https://twitter.com/marcduiker) created the Clippy, Rocky, Zappy, rubber duck, snake, cockatiel, Ferris the crab, and Mod the dotnet bot media assets.

[Elthen](https://twitter.com/pixelthen) created the fox media assets.

[Karen Rustad Tölva](https://www.aldeka.net) designed the original concept of Ferris the crab.

[Kevin Huang](https://github.com/kevin2huang) created the Akita inu media assets.

The turtle animations were designed by enkeefe using [Pixelart](https://www.pixilart.com/draw).

## Thank you

Thanks to all the [contributors](https://github.com/tonybaloney/vscode-pets/graphs/contributors) to this project.
