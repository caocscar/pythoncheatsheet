# Python Cheat Sheet
Notes for Myself

## How to import modules from a different folder than the working directory
To import custom modules (or python scripts) from a different folder than the working directory go to the `..\lib\site-packages` folder of your Python installation. 

For Windows, this is usually under
`..\Continuum\Anaconda3\Lib\site-packages`

For Mac OSX, possible paths include  
`/anaconda/lib/python3.5/site-packages`  
OR  
`/Users/your_name/anaconda/lib/python3.5/site-packages`  
depending on where you installed Anaconda and what it's filename is.

Next, create a new path file called "additional_import_paths.pth" (or whatever). Edit the file to include the path directory you want to search for importing modules. For Mac OSX users, the easiest way to do this would be in terminal:

#go to directory for Anaconda's site-packages
```python
mkdir -p /anaconda/lib/python3.5/site-packages`
cd /anaconda/lib/python3.5/site-packages`

#create a new .pth file
cat >additional_import_paths.pth <<EOF`

#add the path for your module
/Users/module_location

#exit
EOF
```
For Mac OSX users who would like to edit the file after its creation but cannot open the .pth file, download "Text-Wrangler" from the App-Store. Right click on the .pth file and choose: open with > Text-Wrangler. Paste your desired path (wherever your module is) inside and save.

For example:  
`C:\Users\caoa\Box Sync\CMISST\subversion\build_dataset_scripts\trunk`

You may need to restart Python after changing the contents of `additional_import_paths.pth`.

**Note:** No need to add this file to your PATH
