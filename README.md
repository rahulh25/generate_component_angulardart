# Generate Angular Components for Angular Dart
This python script helps you generate a component for your angulardart project (instead of using the traditional ngdart generate component command). This will create the html, css and the dart file with some general boilerplate for the dart and the html file. This also creates a folder in the lib/src folder of your project for the component with all the files, instead of just generally creating the html and dart file in the lib/src folder as done by the ngdart generate component command.

<h6>
<b>Although you can change the folder name by using -p in the ngdart command it does not create the css file and you also have to manually create the subfolder inside the main folder where you wish to create the component. This file is more in line with what the <i>ng generate component</i> command for Angular with typescript feels like. If in future there are any changes in the <i>ngdart generate component</i> command please refer to that. This code will howerver work in any case.</b>

<h5>
<b><i>If you wish to use the command directly just copy the compiled folder to your C drive and add the path to the dist folder in your environment variables</i></b>
</h5>

## Steps to use the script

1. Clone or download the repository on your local machine.
2. Once the you have downloaded the project go into the project folder and open your bash terminal(for MAC/UNIX/LINUX users) or open git bash (for Windows users).
3. Once you open the terminal run the following command:

```bash
cp create-component ~/bin
```

<b>Note: If you get an error in the above command run the below command first:</b>

```bash
mkdir -p ~/bin
```

4. Once you have copied the script to your bin folder run the following command to bin to your path:

```bash
export PATH=$PATH":$HOME/bin"
```

5. Once all the above steps have been executed successfully you can run the following command in your AngularDart project folder tp create a component:

```bash
create-component <component_name> [<subfolder_name>]
```

You will see that it creates a component folder under /lib/src or under /lib/src/subfolder_name with all your html, dart and css files.

## Examples of using the command

<h6>(For Windows make sure you are still running the commands using <i>git bash</i>)</h6>

1. Using it with just the component_name:

```bash
create-component home
```

2. Creating inside a subfolder

```bash
create-component home main
```

3. Creating the component within multiple subfolders

```bash
create-component home main/page
```

## If the above steps do not work

In case the other steps do not work for you follow the following steps <b>(Make sure to run these steps you have the .py extension of your file added)</b>:

1. Install pyinstaller using pip by running the following command:

```bash
pip install pyinstaller
```

<b>NOTE: </b> Make sure you have python version below 3.9 installed on your system as 3.9 gives issues in pip install (This is during the time of the writing of this document).

2. Run the following command inside the folder with the python file:

```bash
pyinstaller --onefile create-component
```

3. Once you run the command it will create the following file structure:

```bash
│   ngdartgc.py
│   ngdartgc.spec
│
├───build
│   └───ngdartgc
├───dist
│       ngdartgc.exe
└───__pycache__
        ngdartgc.cpython-37.pyc
```

3. Copy over all the files mentioned above in a folder inside the C drive or if you wish to keep the file where it is then move forward to the next step
4. Add the path to your dist folder to your environment variables.
5. Now you can run the following command:

```bash
create-component.exe <component_name> [<subfolder_name>]
```

## Examples of using the command with above steps

<h6>(For Windows make sure you are still running the commands using <i>git bash</i>)</h6>

1. Using it with just the component_name:

```bash
create-component.exe home
```

2. Creating inside a subfolder

```bash
create-component.exe home main
```

3. Creating the component within multiple subfolders

```bash
create-component.exe home main/page
```

## Note

If you wish to create your own name for the command instead of <b><i>create-component</i></b> command then once you clone/download the repository you can change the python(create-component) file name and give it whatever name you like and you can call that command(file name) when creating the components

## Reference

1. Making command line python script <br>
   https://dbader.org/blog/how-to-make-command-line-commands-with-python

2. Download git bash for windows <br>
   https://git-scm.com/downloads
    
3. Create Python Executable file <br>
   https://datatofish.com/executable-pyinstaller/


