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

We are generating 4 differents pages in subfolder of the `docs/` folder. The folder where the documentation will be generated needs to exist:

```bash
mkdir -p docs/summary
ontospy gendocs -o docs/summary --type 1 --nobrowser ontologies/audioset.rdf
# >1

mkdir -p docs/browse
ontospy gendocs -o docs/browse --type 2 --nobrowser ontologies/audioset.rdf
# >2

mkdir -p docs/classtree
ontospy gendocs -o docs/classtree --type 4 --nobrowser ontologies/audioset.rdf
# >4

mkdir -p docs/graph
ontospy gendocs -o docs/graph --type 10 --nobrowser ontologies/audioset.rdf
# >10
```

> See the source code for [more details on parameters](https://github.com/lambdamusic/Ontospy/blob/master/ontospy/cli.py#L169).

The Graph visualisation can be improved at:
* https://github.com/lambdamusic/Ontospy/blob/master/ontospy/ontodocs/viz/viz_html_multi.py
* https://github.com/lambdamusic/Ontospy/blob/master/ontospy/ontodocs/media/templates/misc/sigmajs.html

### See also

[WebVOWL](http://www.visualdataweb.de/webvowl/), d3.js graph viewer: 

http://www.visualdataweb.de/webvowl/#iri=https://raw.githubusercontent.com/MaastrichtU-IDS/ontology-editor-audioset/master/ontologies/audioset.rdf

### Original AudioSet Ontology license

The ontology is made available by Google Inc. under a Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license.
