After configuring Git and creating a private repository, proceed as follows:

1. Navigate to a local drive (for example, D:\) and right-click inside it.

2. Select Git Bash Here from the context menu.

3. In the terminal, run:
    ```bash
        git clone git@github.com:<your-username>/<your-repository-name>.git
    ```

Then press Enter.

4. If this is your first time cloning from GitHub, you may be prompted to authorize the SSH connection. Type Yes and press Enter.

5. Once cloning completes, a new folder with the repository name will appear.

6. Open this folder and verify that it contains a hidden .git directory.

7. In the same directory run:
    ```bash
        git-crypt init
        git-crypt export-key keyfile
    ```
8. Move the keyfile in a secure location away from this folder.

9. Copy the pre-commit and post-commit hook files into the .git/hooks directory (ensure hidden folders are visible).

10. Copy the .gitignore and .gitattributes from this repository's docs folder into your repository folder (the one containing .git).

11. Launch Logseq and add this repository folder (the one containing .git) as a new graph.

12. In Logseq, go to Settings → Version Control and enable Git auto commit.

13. Make a small change in Logseq and wait a few minutes to confirm that the update appears on GitHub.

If everything works as expected, your Logseq–GitHub synchronization is successfully set up.