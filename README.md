# FDS

FDS or *Folder Downloader System* is a version system for you're game, or project, a little like minecraft or a version saver. 

**IT'S NOT LIKE GIT, IT'S ONLY FOR VERSION SAVE, RELEASE, OR THINGS LIKE THAT**

* [Documentation](https://mistermine01.github.io/FDS/)

## How use it

### Use Client

* First copy php server in a web server
    * Copy fdf_folder and fdv_folder. Point it in ```properties.json```.
    ```json
    {
	    "fdf_folder": "fdf",
	    "fdv_folder": "version"
    }
    ```
    * Get the adress
* in your python code call the class.
    ```python
    import fds
    Server = fds.FDSServer("URL")
    Client = fds.FDSClient("src", "version", Server)
    ```

### Use Compiler

```python
import fds

Compiler = fds.FDSCompiler(
    "dependency.fdd",
    "fdf_folder",
    "version_folder")
Compiler.create_new_version("1.0", "folder")
```