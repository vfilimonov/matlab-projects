matlab-projects
===============

The missing projects manager for MATLAB

PROJECTS(cmd, projectName) manages current working directory and files that are opened in MATLAB editor (but not the workspace). 
Available commands are: 
'list', 'show', 'save', 'load', 'close', 'rename', 'delete', 'active'

PROJECTS or
PROJECTS('list') shows all stored projects. Arrow marks active project.

PROJECTS('active') returns the name of the active project

PROJECTS('show') shows information about the current project
PROJECTS('show', project_name) shows information about the project

PROJECTS('close') closes all opened files

PROJECTS('save') saves current working directory and editor state under the active project 
PROJECTS('save', projectName) saves current working directory and editor state under the specified project name

PROJECTS('load') restores the project "default" 
PROJECTS('load', projectName) restores the project with specified name

PROJECTS('open') is synonym for PROJECTS('load')

PROJECTS('rename', newName) renames the active project
PROJECTS('rename', projectName, newName) renames the project

PROJECTS('delete') deletes the active project
PROJECTS('delete', projectName) deletes the project with specified name

Examples:
  projects list
  projects save myProject
  projects close
  projects load default
  projects rename myProject myLibrary

All projects are stored in the %userpath%/projects.mat. This file with the empty "default" project is created at the first run of the script.

First project always has name "default"
