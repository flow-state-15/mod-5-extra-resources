# CodeSandbox FAQs
## Table of Contents

 - [How can I save a Github repo as a sandbox?](https://github.com/flow-state-15/mod-5-extra-resources/blob/main/resources/codesandbox-FAQs.md#how-can-i-save-a-github-repo-as-a-sandbox)
 - [My files are not saving?](https://github.com/flow-state-15/mod-5-extra-resources/blob/main/resources/codesandbox-FAQs.md#my-files-are-not-saving)
 - [How do I stop my code if its stuck in an infinite loop?](https://github.com/flow-state-15/mod-5-extra-resources/blob/main/resources/codesandbox-FAQs.md#how-do-i-stop-my-code-if-its-stuck-in-an-infinite-loop)
 - [How do I see React DevTools?](https://github.com/flow-state-15/mod-5-extra-resources/blob/main/resources/codesandbox-FAQs.md#how-do-i-see-react-devtools)
 - [I don't see my file structure or side navigation buttons, how do I get it back?](https://github.com/flow-state-15/mod-5-extra-resources/blob/main/resources/codesandbox-FAQs.md#i-dont-see-my-file-structure-or-side-navigation-buttons-how-do-i-get-it-back)
---------------------------
## How can I save a Github repo as a sandbox?
1. **While on the Github repo, in the URL, add "box" after "github".** The browser will reload the repo in CodeSandbox.
    - *Example:* `https://githubbox.com/appacademy/...`
2. **Make sure you are logged in to your own account so you can save your progress!** 
    - To register, click "Sign In" or go to https://codesandbox.io/signin and sign in using your Github or Google account. 
3. **Click `File` --> `Save As`..** 
4. **Click Enter on the next popup.**
    - ![/App.js popup screenshot](https://user-images.githubusercontent.com/89945390/194419740-5bd7af82-637d-4a55-ab40-fa9a75b4f47f.png)
5. After it reloads, it will assign a random name to the file and it will be placed in `Drafts`:
    - *Example:*  
    - ![drafts and random name "jolly-parm-16dm5r" screenshot](https://user-images.githubusercontent.com/89945390/194420301-bc64b9ca-4894-406e-8645-5adf0d2691ca.png)
6. **Click the random name and change it to the name of the practice.** 
7. **Click on `Drafts` to the left of the name to move the file to a new folder** (`Drafts` is only temporary).
   - ![move 1 item screenshot](https://user-images.githubusercontent.com/89945390/194420815-8c402d38-7dc0-4596-836d-1e7e2f0ca6d9.png)
   - Either select `All Sandboxes` or an already created folder to store it in. 
   - Right-clicking will allow you to create a folder, too. 
-----------------------
## My files are not saving?
1. **Transfer any code you have written in the current file outside of CodeSandbox, like a Google Document or Notepad.**
2. **Hard refresh your browser.** 
    - *Chrome & Firefox:*
	    - Windows: Hold **Ctrl** and then press the "Reload" button OR **F5**
	    - Mac: Hold **Cmd** +**Shift** and then press the "Reload" button OR **R**
3. **Test after Saving now.**
    - *Still not working?* Please try to screen record the behavior and contact us. 
-----------------------
## How do I stop my code if its stuck in an infinite loop?
1. **Make sure that *Infinite Loop Protection* is on in your configuration files. Click Edit on 'sandbox.config.json' to see this option.**
    - However, this protection doesn't work for everything, especially in incomplete code. 
![screenshot of Config file settings](https://user-images.githubusercontent.com/89945390/194360968-cd825e99-975b-4149-9d54-9e5cb0db7b3f.png)
2. **If your file is still frozen and you can't edit:** 
    - Append `runonclick=1` to the editor URL to stop the code from being automatically executed enabling you to edit your code to resolve it.
        - For example: "https://codesandbox.io/s/new?runonclick=1"

----------------------------
## How do I see React DevTools?
There are a couple ways to see the React DevTools. 
1. **The built-in Browser tab has the React DevTools at the bottom.**
![View of CodeSandbox with console and react devtools squared](../assets/images/readme-screenshots/codesandbox-console-reactdevtools-view-1.png)
    - #1 is where you can see the browser's console & #2 is how you see the React DevTools. 
    - Sometimes the React DevTools here take a while to load, so use the next option if it gives you trouble. ⤵
2. **The right-most button on the Browser tab has an "Open In New Window" where you can have it fullscreen.**
    - ![View of CodeSandbox browser's Open in New Window button](../assets/images/readme-screenshots/codesandbox-open-new-window.png)
    - Next, open up the inspect tool! (Right-click then "Inspect" in the opened window) 
    - Navigate to the "Components" tab!
    - ![View of Components React DevTool in Browser Inspect](../assets/images/readme-screenshots/codesandbox-opened-dev-tools.png)

----------------------------

## I don't see my file structure or side navigation buttons, how do I get it back?
**You might accidentally be in the *Projects Beta*:**
 1. **Travel back to the Dashboard.**
    - ![Project Beta logo screenshot](https://user-images.githubusercontent.com/89945390/194381684-9088c7e7-1aff-4ebc-813f-cdeb136129ec.png)
 2. **If you see you are in the *Projects Beta* view, on the bottom left, click "Go to Sandboxes".**
     - ![go to sandboxes screenshot](https://user-images.githubusercontent.com/89945390/194381982-eb142ad8-d021-43d3-b012-e8870f3e6a68.png)

-----------------------------
[Back to top ⤴](https://github.com/flow-state-15/mod-5-extra-resources/blob/main/resources/codesandbox-FAQs.md#codesandbox-faqs)
