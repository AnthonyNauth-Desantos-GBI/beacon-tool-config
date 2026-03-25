# Rezolve Beacons Identifier Error Validation Config File

Used by the Rezolve Beacons Identifier Extension(WIP) to validate beacons

The JSON file is used to provide validation tests on the incoming beacons and provide necessary responses for the user including details on how to resolve the errors.

## Available Fields

In this config you may call variables to compare by using the `$` like so `$beacon` 
This will grant you access to the variable context as porovided by the extension. 

As of Version 1.2.0 fields available are as follows

- $beacon
    -- Includes all fields of the Beacon Response JSON in the format they appear in the response. eg. you can access Login ID by using $beacon.visit.customerData.loginId see Rezolve Customer Beacon docs for more details
- $tracker
    -- Includes the tracker data such as the script used to dertermine the tracker's version
- $beaconOriginCount
    -- Includes a numeric value of the number of Beacon Origin fields are set to true

## Comparitors

There are currenlty 2 methods for comparing values

- number_compare
used to compare direct number values and numeric variables. you may use the following to compare values as needed.
   -- "<" value on left is less than the right
   -- ">" value on left is greater than the right
   -- "<=" value on left is less or equal to value on the right
   -- ">=" value on left is greater or equal to value on the right
   -- "%" value on left divided by value on the right contains remainder(if divisible will be false, if there is a remainder will return true)
   -- "==" value on left is equal to value on the right

- string_compare
   Compares the string value as is unmodified if they are equal will return true

## How to Update

---

### Using the Terminal

1. **Clone the repository (first time only):**  
   `git clone https://github.com/AnthonyNauth-Desantos-GBI/beacon-tool-config.git`

2. **Navigate into the repository:(only needed if file loaded into subdirectory)**  
   `cd {subdirectory}`

3. **Switch to `main` and pull the latest changes:**  
   `git checkout main`  
   `git pull origin main`

4. **Create and switch to a new branch:**  
   `git checkout -b feature-branch-name`

5. **Make your changes, then stage and commit them:**  
   `git add .`  
   `git commit -m "Describe your changes"`

6. **Push the new branch to GitHub:**  
   `git push -u origin feature-branch-name`

7. **Create a pull request on GitHub:**  
   - Go to the repository page on GitHub.  
   - Click **Compare & pull request**.  
   - Ensure the base branch is `main`.  
   - Click **Create pull request**.

8. **Merge the pull request:**  (Completed by Admin)
   - On the PR page, click **Merge pull request** → **Confirm merge**.

---

### Using GitHub Desktop

1. **Clone the repository (first time only):**  
   - Open GitHub Desktop → **File** → **Clone repository…**  
   - Select **Example Repo** and clone it.

2. **Switch to and update `main`:**  
   - Click **Current branch** → choose `main`.  
   - Click **Fetch origin**.

3. **Create a new branch:**  
   - Click **Current branch** → **New branch…**  
   - Name it (e.g., `feature-branch-name`) → **Create branch**.

4. **Make your changes and commit them:**  
   - Edit files in your code editor.  
   - In GitHub Desktop, review the **Changes** tab.  
   - Add a summary → click **Commit to feature-branch-name**.

5. **Publish the branch:**  
   - Click **Publish branch** in the top bar.

6. **Create a pull request:**  
   - Click **Create Pull Request** in GitHub Desktop.  
   - GitHub will open in your browser → click **Create pull request**.

7. **Merge the pull request:**  (Completed by Admin)
   - On GitHub, click **Merge pull request** → **Confirm merge**.