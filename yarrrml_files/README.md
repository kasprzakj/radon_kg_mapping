How to use what's in here?

1. Clone this repository.
2. Download [RMLmapper](https://github.com/RMLio/rmlmapper-java) and [yarrrml-parser](https://github.com/RMLio/yarrrml-parser).
3. If you don't have it yet, download necessary data, for example using [get_data.ipynb](https://github.com/kasprzakj/radon_kg_mapping/tree/main/data_acquisition/get_data.ipynb) into `data/{dataset_name}.json` as per the current example in `get_data.ipynb`.
4. If you've made changes/created a new yarrrml file, it should be placed in this folder.
5. Open command line in the root project folder.
6. Run `yarrrml-parser -i yarrrml_files/combined.yml -o mappings/combined.rml.ttl`.
7. Run `java -jar rmlmapper.jar -m mappings/combined.rml.ttl -o turtles/combined.ttl -s turtle`.
8. You should now have a the `combined.ttl` file in `turtles`.
9. If you want to split the file into multiple smaller files, run the code in `data_acquisition/turtle_split.ipynb`