# Sample Project for documentation-builds

## The Idea
An example documentation how to setup generated documentation with tecton, markdown and host in kubernetes

The idea behind this project is, that projects need some kind of architecture and operations-documentation. In good cases this is already available as [Markdown](https://www.markdownguide.org/) documents in a separate repository or reside in the same repository as the project.
The typical needs are, to make this documentation available for colleagues, stakeholders and operations-teams.

Therefore I want to:

* Setup a pipeline with [Tekton](https://tekton.dev/)
* Use [Mkdocs](https://www.mkdocs.org/) to create static pages 
* and [Mermaid](https://whatismarkdown.com/how-to-use-mermaid-to-create-diagrams-in-markdown/) to render the graphs
* then create a [docker](https://www.docker.com/) container as server
* and run it in a local [kubernetes](https://kubernetes.io/de/)

At each step the setup can be stopped, e.g. you can use the generated static pages to host them wherever you want, or you do generate a docker container and host this one somewhere else without kubernetes.

