# obsidian-template

Obsidian template that I used daily for work. It is based around the usage of templater to easily create new notes with the correct structure, an the dataview plugin to show relevant relation pages when searching for various concepts, projects and people.

My main goal with this template was to find a good comprise between a folder-based approach, and a link-based approach. I try to add as many links as possible between the concepts, making sure that notes are correctly linked to a Project, a Person, a Company, etc. This allows me to easily navigate between the notes, and to quickly find all notes related to a specific topic.

While strictly not necessary for Obsidian, I still use a folder per project, allowing me to easily archive a full project, and for easy sharing of all project notes with collegues. However, concepts, people and companies are all in the same `Knowledge` folder, as they are not project specific and can be reused across them.

## Folder structure

This is the template for my Obsidian notes at work. It is organized as follows:
- `Projects`: One folder per project, with the company and project name as the folder name. Each project folder contains:
  - `Company - Project.md`  : the main file for the project, containg the overview
  - `Meetings`: One file per meeting, with the meeting name and date as the file name
  - `Notes`: One file per note, with the company and note name as the file name
  - `Topics`: One file per topic, with the topic name as the file name

- `Archive`: When a project is finished, I move its folder from the `Projects` folder to the `Archive` folder.
- `Knowledge
  - `Companies`: One file per company
  - `Concepts`: One file per concept
  - `People`: One file per person
- `Media`: Used to store images, that I reuse across mutliple projects (e.g. icons)
- `Agenda`: Contains one file per day, with the date as the file name. This is where I keep my daily notes, giving me an overview of what I did each day and active tasks.
- `Templates`: Contains the templates files 

## How to use

My main interaciton is through the ctrl-N (cmd-N on Mac) shortcut to create a new note. I then select the template I want to use, and it asks me for various information depending on the type of note. 

- `Company`: Asks for the Company Name
- `Person`: Asks for the Company, First Name and Last Name
- `Project`: Asks the the Company and Project Name
- `Note`: Asks for the Project and Note name
- `Meeting`: Asks for the Project and Meeting name
- `Concept`: Asks for the Concept name
- `Topic`: Asks for the Project and Topic name

The files will automatically be created in the correct folder, with the correct name. Folders are created automatically if they don't exist yet.
When adding attachements like images or escalidraw diagrams, they will be automatically added to a `_attachments` folder in the same folder as the note.

## Plugins

- Advanced Tables: For easier usage of markdown tables
- Calendar: For easy access to the daily notes
- Custom File Explorer Sorting: To keep the folders in the correct order
- Dataview: For all queries in the various overview pages
- Escalidraw: My prefered drawing tool for obsidian. I use the ctrl+alt+D to create an embedded a new drawing in the current note.
- Folder Note: To automatically create open the main folder note when opening a folder
- Iconize: To add icons to the folders
- Minimal Theme Settings: additonal settings for the minimal theme that I use
- Recent File: Quick access to recently opened files
- Style Settings: Additional settings to control the style, allowing for instance the double column layout in the daily notes.
- Tag Wrangler: For easier tag management, including bulk renaming
- Tasks: Allow the creation of tasks with due dates, and easier checking of tasks in progress or done
- Templater: For the creation of new notes with templates


