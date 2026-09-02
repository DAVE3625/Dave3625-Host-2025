# Mini UV Troubleshooting Helper
*This is a super simple and non-formal helper that may help in debugging your uv setup.*

When picking a kernel, you’re looking for something like
`LabX/.venv/bin/python`

## If the kernel doesn't show up
1. Open the Command Palette by doing this:
   - Mac: `cmd + shift + p`  
   - Windows: `ctrl + shift + p` (or `F1`)  

2. Find and run the command **Python: Select Interpreter**  
   - If your `uv` environment (e.g. `Lab2/.venv/bin/python`) is there, choose it!  
   - If not, keep troubleshooting

## Try the following (in order)
1. Close and reopen the notebook (e.g. `lab0.ipynb`)
2. Restart VS Code
3. Command Palette again, this time run **Jupyter: Clear Jupyter Server Kernel Cache**.  
4. Did you initialize `uv` in the correct directory?  
   - Each lab should have its own `.venv` unless you want one shared env (which we don't generally recommend) 

## A UV kernel shows up, but it's for another lab 
That means VS Code found another `.venv` you created maybe in a parent folder or another lab.  
Check if you were inside the correct lab folder when you ran `uv init`! 

To do this, look at your file hierarchy on the left side of VS Code. 

#### Which folder is the file called `uv.lock`is located in?

This should be the same as the lab you are working on if it was initialized correctly. 

#### Is it in a parent folder?

VS Code can't tell the difference between the right and wrong uv environments. Try initalizing it in the right directory. 

## How do I remove the wrong one?

1. Navigate to the folder where you want to remove uv
2. Run the following commands

    ```bash
    rm -rf .venv
    rm pyproject.toml
    ```
    
3. Find the wrong kernel 

    ```bash
    jupyter kernelspec list    # find the one pointing to the wrong .venv
    jupyter kernelspec uninstall <kernel-name>
    ```

4. Reinitialize it in the right place


## Still stuck?
Make sure your env has a kernel installed:  
```bash
uv add ipykernel
python -m ipykernel install --user --name labX --display-name "Python (labX)"
```

## ... still stuck?
Contact us and we'll help you!

