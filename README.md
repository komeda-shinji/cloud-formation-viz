cloud-formation-viz
===================

This tool is for creating visualizations of CloudFormation templates.
It outputs Graphviz dot files. It can be used like this:

```` bash
cat example.template | ./cfviz | dot -Tsvg -oexample.svg
````

The only dependency of the `cfviz` script is Python. You will also
need to have [Graphviz] [graphviz] installed for the output to be any
use.

The [samples] [samples] directory contains output of running the tool
over the [samples] [aws-samples] provided by AWS.

[aws-samples]: http://aws.amazon.com/cloudformation/aws-cloudformation-templates/
[graphviz]: http://www.graphviz.org/
[samples]: https://github.com/benbc/cloud-formation-viz/tree/master/samples

cfgraphml
===================

The `cfgraphml` script was created based on cfviz and [dottoxml].
My fork dottoxml repository can be found [here] [dottoxml_fork].

This tool is for creating visualizations of CloudFormation templates.
It outputs GraphML file. It can be used like this:

```` bash
cfgraphml [options] infile.template outfile.graphml
````

Plaese get the [AWS simple icons] [AWS_simple_icons], and extract it into `simple-icons`.

[AWS_simple_icons]: https://aws.amazon.com/jp/architecture/icons/

The `cfgraphml` script need Python, [networkx], and [Graphviz].
It requires further either [pydot] and [pygraphviz].

[networkx]: https://networkx.github.io
[pydot]: https://pypi.python.org/pypi/pydot
[pygraphviz]: https://pygraphviz.github.io
[dottoxml]: https://bitbucket.org/dirkbaechle/dottoxml
[dottoxml_fork]: https://bitbucket.org/komeda_shinji/dottoxml

You can edit the output with [yEd], and create a PNG or SVG output to be any use.

[yEd]: https://www.yworks.com/products/yed
