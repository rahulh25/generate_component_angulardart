# Generate Angular Components for Angular Dart
This python script helps you generate a component for your angulardart project (instead of using the traditional ngdart generate component command). This will create the html, css and the dart file with some general boilerplate for the dart and the html file. This also creates a folder in the lib/src folder of your project for the component with all the files, instead of just generally creating the html and dart file in the lib/src folder as done by the ngdart generate component command.

<b>PS:</b> Although you can change the folder name by using -p in the ngdart command it does not create the css file and also creates a /lib/src folder inside the folder where you wish to create the component. This file is more in line with what the <i>ng generate component</i> command for Angular with typescript feels like. 

<b>If in future there are any changes in the <i>ngdart generate component</i> command please refer to that. This code will howerver work in that case as well.</b>

## Steps to use the script

1. Clone or download the repository on your local machine.
2. Once the you have downloaded the project go into the project folder and open your bash terminal(for MAC/UNIX/LINUX users) or open git bash (for Windows users).
3. Once you open the terminal run the following command:

```bash
cp myecho ~/bin
```

Note: If you get an error in the above command run the below command first:

```bash
mkdir -p ~/bin
```

4. Once you have copied the script to your bin folder run the following command to bin to your path:

```bash
export PATH=$PATH":$HOME/bin"
```

5. Once all the above steps have been executed successfully you can run the following command in your AngularDart project folder tp create a component:

```bash
createcomp <component_name>
```

You will see that it creates a component folder under /lib/src with all your html, dart and css files.

## Note

If you wish to create your own name for the command instead of <b><i>createcomp</i></b> command then once you clone/download the repository you can change the python(createcomp) file name and give it whatever name you like and you can call that command(file name) when creating the components

## Reference

1. Making command line python script <br>
    https://dbader.org/blog/how-to-make-command-line-commands-with-python

2. Download git bash for windows <br>
    https://git-scm.com/downloads


