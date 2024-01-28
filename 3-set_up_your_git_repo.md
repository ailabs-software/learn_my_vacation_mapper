# Set up your git repo

**Goal:** At the end of this section, you'll have our code hosted in a git repo.



So that I can help check your work, it is a good idea to setup a hosted git repo, such as on GitHub.

I have provided instructions here for Github.



#### Setting up a git repo hosted in Github

If you are using another service you prefer to host your git repo, that's fine.

Creating a new GitHub repository from an existing directory involves a few steps. Here's a general guide to help you through the process:

1. **Initialise a Git Repository in Your Directory:** First, you need to initialize a Git repository in your local directory. Open a terminal or command prompt and navigate to your project directory. Then run:

   ```
   git init
   ```

2. **Add Your Files to the Repository:** To add all files in the directory to the repository, use:

   ```
   git add .
   ```

   This command stages all your files for committing. Replace `.` with specific file names if you only want to add certain files.

3. **Commit Your Files:** Commit the staged files with a message describing the initial state of the repository:

   ```
   git commit -m "Initial commit"
   ```

4. **Create a New Repository on GitHub:**

   - Go to [GitHub](https://github.com/) and sign in.

   - Click the "+" icon in the upper right corner and select "New repository".

   - Fill out the form with your repository details (like name, description, visibility).

     Click "Create repository".

5. **Link Your Local Repository to the GitHub Repository:**

   - On the new repository page on GitHub, you'll find a URL under "Quick setup". Copy this URL.

   - Back in your terminal, link your local repository to the GitHub one with:

     ```
     git remote add origin [URL]
     ```

     Replace 

     ```
     [URL]
     ```

      with the URL you copied from GitHub.

6. **Push Your Local Repository to GitHub:** Finally, push your local repository to GitHub with:

   ```
   git push -u origin master
   ```

   If you're using a branch other than `master`, replace `master` with your branch name.

7. **Verify:** After pushing, refresh your GitHub repository page to see your files there.

Remember, if your project is sensitive or private, make sure to set your GitHub repository to private during the creation process. Also, if you have large files or many files, you might need to look into .gitignore files or Git LFS (Large File Storage).
