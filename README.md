# ontology-editor-audioset
A Jupyter Notebook to edit the AudioSet ontology

* [AudioSet "ontology" GitHub repository](https://github.com/audioset/ontology)
* [AudioSet Ontology](https://research.google.com/audioset///ontology/index.html)
* [Owlready2 documentation](https://owlready2.readthedocs.io/en/latest/)
* The AudioSet ontology is licensed by Google Inc. under https://creativecommons.org/licenses/by-sa/4.0/

### Start JupyterLab

Start JupyterLab locally from the root folder of the git repository:

```bash
docker run --rm -it -p 8888:8888 -v $(pwd):/notebooks -e PASSWORD="<your_secret>" umids/jupyterlab:latest
```

### Generate docs

See Ontospy documentation: http://lambdamusic.github.io/Ontospy

Install Ontospy:

```bash
pip install ontospy[FULL]
```

Using Ontospy, from the commandline:

```bash
ontospy gendocs -o docs https://raw.githubusercontent.com/MaastrichtU-IDS/ontology-editor-audioset/master/ontologies/audioset.rdf
```

> Choose the visualization type

We are generating 3 differents pages in subfolder of the `docs/` folder. The folder where the documentation will be generated needs to exist:

```bash
mkdir -p docs/summary
ontospy gendocs -o docs/summary https://raw.githubusercontent.com/MaastrichtU-IDS/ontology-editor-audioset/master/ontologies/audioset.rdf
# 1

mkdir -p docs/browse
ontospy gendocs -o docs/browse https://raw.githubusercontent.com/MaastrichtU-IDS/ontology-editor-audioset/master/ontologies/audioset.rdf
# 2

mkdir -p docs/classtree
ontospy gendocs -o docs/classtree https://raw.githubusercontent.com/MaastrichtU-IDS/ontology-editor-audioset/master/ontologies/audioset.rdf
# 4
```

### See also

[WebVOWL](http://www.visualdataweb.de/webvowl/), d3.js graph viewer: 

http://www.visualdataweb.de/webvowl/#iri=https://raw.githubusercontent.com/MaastrichtU-IDS/ontology-editor-audioset/master/ontologies/audioset.rdf

### Original AudioSet Ontology license

The ontology is made available by Google Inc. under a Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license.
