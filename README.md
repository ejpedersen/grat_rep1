### Why I changed the GitHub structure

JATOS has defaults that make it difficult to build a study from a sub-folder of a larger project. This is somewhat difficult to articulate, but the JATOS structure needs to match the file structure of the GitHub repo if we want to collaborate this way.

We should all take the following steps on our local machines:

*In JATOS*

1. Create a 'New Study' and call it 'grat_rep1'.

* This will create a folder within `study_assets_root` called `grat_rep1`.

2. Delete the folder created by JATOS.

*In ATOM*

3. Open the `study_assets_root` folder.

4. Clone the GitHub repo from https://github.com/ejpedersen/grat_rep1

Now JATOS and GitHub will be referencing the same working directory on your folder. This will make collaborating on code seamless. Without taking these steps, you would have to drag changed files from the repository into the folder created in `study_assets_root`. That's no fun. Now all you have to do to get JATOS to recognize the most recent version is to use `git pull`.