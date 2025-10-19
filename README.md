# Motivation

I'd like to develop a system to track notes, projects, and tasks.

As my workload increases and becomes more varied, I find difficulty keeping track of everything I need to continue working. At the most basic level, this is just a general need for storing generic information, but there are obvious categories:

Notes - Basic knowledge that can be used to synthesize further conclusions. Any piece of knowledge that isn't a direct action would almost certainly be a note.

Tasks - A simple instruction. Not necessarily atomic, but has a clear scope and goal

Projects - Collections of tasks and notes that serve a common goal. More open-ended than individual tasks

Workflows - Common sequences of tasks that can be generalized and applied to fit a variety of needs.

Something I've found difficult about forming a good system is how these pieces relate to each other. I'd love a system that helped me quickly identify past knowledge from other projects or integrate the knowledge learned from a finished project into a central repository. It would be incredibly rewarding to automate the task of categorizing and storing this knowledge as well.

Much like how Wikipedia contains links to prerequisite knowledge, I'd like a system that can (ideally automatically) allow new pages/notes/posts to reference previously noted material.

# Requirements

A bare minimum working version should probably include the following:

- Manage a collection of 'notes'
    - For now, a note can just be a text file
- User can search for a term in the collection

Further features would include:

- Marking notes as belonging to some category (task, project, workflow)
- User can link to other notes
- Cool terminal UI to search and follow links
- User can make overview pages for common terms
- User can jump to the overview page for a term selected in some other page
- Smarter search (multiple terms, exclude terms, etc.)
- Some way to compile task notes into a TODO page

# Research

## Fancy Terminal Programs

[kilo](https://viewsourcecode.org/snaptoken/kilo/index.html)

## Task Organization

[Kanban](https://en.wikipedia.org/wiki/Kanban)

## Note Organization