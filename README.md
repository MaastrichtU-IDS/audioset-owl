# ontology-editor-audioset
A Jupyter Notebook to edit the AudioSet ontology

* [AudioSet "ontology" GitHub repository](https://github.com/audioset/ontology)
* [AudioSet Ontology](https://research.google.com/audioset///ontology/index.html)
* [Owlready2 documentation](https://owlready2.readthedocs.io/en/latest/)

### Start JupyterLab

Start JupyterLab locally from the root folder of the git repository:

```bash
docker run --rm -it -p 8888:8888 -v $(pwd):/notebooks -e PASSWORD="<your_secret>" umids/jupyterlab:latest
```

