# User manual with guides

## 1. How to load dependencies

- to load the dependencies execute "mvn package"
    - in the "/target" directory there should now be the following files:
        - "depedency-tree.json"
        - "dependency-tree.dot"
        - "dependencies.png"
        - "change-log.json" (only if a change via details view was already made)
- in the Overview tab you can find a "load dependencies" Button, which loads the dependencies from the target directory
  into the plugin

## 2. Overview panel

- here you can see some statistics about the loaded dependencies
- there are two buttons:
    - "Load dependencies" which loads the new dependencies whenever "mvn package" was executed
    - "Open Logs" which opens the log file and shows any changes made to the dependencies

## 3. Dependency Manager

- tree view of the dependencies
- search bar to search directly for specific dependencies
- filter dropdown to filter the dependencies for:
    - "None" no filter
    - "omitted" depencies (dependency version being cutoff by the maven version mediation
    - "unused" dependencies (dependency not used in the project) **NOT REALLY RELIABLE!!**
    - "used" dependencies (dependency used in the project) **NOT REALLY RELIABLE!!**
- **double click on a dependency** to open the dependency detail view

### 3.1 Dependency detail view

- shows information about the specific dependency:
    - GroupID
    - ArtifactID
    - Scope
    - path to dependency (in file system)
    - tree label (label as shown in plugin tree view)
    - omitted flag
    - (potentially) unused flag
- "Open Dependency in File Explorer" Button to open the dependency in the file explorer (to find pom file or library)
- "Open used Dependency details" (only if omitted Dependency) opens the detail view of the dependency version that is
  currently being used in programm
- "Use omitted version" (only if omitted Dependency) Button to change the dependency version in the project to the specified dependency version
- "Delete unused Button" (only if unused Dependency) deletes the dependency from the project **CAREFUL: MIGHT BE A FALSE POSTIVE**
- Parent Dependencies Tab shows all parent dependencies of the dependency
- Child Dependencies Tab shows all child dependencies of the dependency
    - **double click on a parent/child dependency** to open the dependency detail view

## 4. Dependency Graph
- shows the dependency tree of the project
- "zoom in/out" button and "fit" button to zoom in/out on the graph

## 5. Tips
- If you want to reload Poject dependencies with new changes, you can execute "mvn package"
- If you want to undo all changes made to the dependencies, you can execute "mvn clean"
- All changes are logged in "/target/change-log.json" file
- unused dependency parsing is not reliable, so it might be wrong sometimes mostly false positives no false negatives