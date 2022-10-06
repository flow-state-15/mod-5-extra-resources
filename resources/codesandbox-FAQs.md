# CodeSandbox FAQs
## Table of Contents

 - How can I save a Github repo as a sandbox?
 - My files are not saving?
 - How do I stop my code if its stuck in an infinite loop?
 - I don't see my file structure or side navigation buttons, how do I get it back?
---------------------------
## How can I save a Github repo as a sandbox?
1. **While on the Github repo, in the URL, add "box" after "github".** The browser will reload the repo in CodeSandbox.
    - *Example:* `https://githubbox.com/appacademy/...`
2. **Click `File` --> `Save As`..** 
3. **Click Enter on the next popup.**
    - ![/App.js popup screenshot](https://user-images.githubusercontent.com/89945390/194419740-5bd7af82-637d-4a55-ab40-fa9a75b4f47f.png)
4. After it reloads, it will assign a random name to the file and it will be placed in `Drafts`:
    - *Example:*  
    - ![drafts and random name "jolly-parm-16dm5r" screenshot](https://user-images.githubusercontent.com/89945390/194420301-bc64b9ca-4894-406e-8645-5adf0d2691ca.png)
5. **Click the random name and change it to the name of the practice.** 
6. **Click on `Drafts` to the left of the name to move the file to a new folder** (`Drafts` is only temporary).
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

## I don't see my file structure or side navigation buttons, how do I get it back?
**You might accidentally be in the *Projects Beta*:**
 1. **Travel back to the Dashboard.**
    - ![Project Beta logo screenshot](https://user-images.githubusercontent.com/89945390/194381684-9088c7e7-1aff-4ebc-813f-cdeb136129ec.png)
 2. **If you see you are in the *Projects Beta* view, on the bottom left, click "Go to Sandboxes".**
     - ![go to sandboxes screenshot](https://user-images.githubusercontent.com/89945390/194381982-eb142ad8-d021-43d3-b012-e8870f3e6a68.png)
