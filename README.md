1. Create a new file named `cloc-git`:
    ```bash
    touch cloc-git
    ```

2. Open the file in Vim to edit:
    ```bash
    vim cloc-git
    ```

3. Copy and paste the following content into the file, then save and exit by typing `:wq` and pressing Enter:
    ```bash
    !/usr/bin/env bash
    git clone --depth 1 "$1" temp-linecount-repo &&
    printf "('temp-linecount-repo' will be deleted automatically)\n\n\n" &&
    cloc temp-linecount-repo &&
    rm -rf temp-linecount-repo
    ```

4. Make the script executable:
    ```bash
    sudo chmod 777 cloc-git
    ```

5. Run the script with the GitHub repository URL and append the output to `git-repo-statistics.txt`:
    ```bash
    ./cloc-git https://github.com/<organization_name>/<repo_name>.git >> git-repo-statistics.txt
    ```

6. List the files in the directory with detailed information:
    ```bash
    ls -la
    ```

7. See details.
    ```bash
    cat git-repo-statistics.tsx
    ```
