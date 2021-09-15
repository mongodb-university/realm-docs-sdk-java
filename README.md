# Yokedox Javadoc Development Testing Repo

First, clone and build Yokedox: https://github.com/mongodb-university/yokedox

To generate docs, run the following in this directory:

```sh
node path/to/yokedox/cli/build/main run \
  -o source \
  --debugGeneratorResultPath ./javadoc \
  --outputMdastJson=0 \
  javadoc
```

- `node path/to/yokedox/cli/build/main run`: run the version of Yokedox you built locally.
- `-o source`: output to the `source/` directory ("source" as in "consumed by snooty")
- `-debugGeneratorResultPath ./javadoc`: consume the generator (javadoc) result from the `javadoc/` directory. This is provided so that you don't have to actually set up Javadoc or clone the realm-java repository to work with Yokedox.
- `--outputMdastJson=0`: by default (for now), Yokedox outputs yokedast json files. You can use these to inspect the output and debug. However, they don't serve any purpose for snooty, so they should not be committed. Remove this line if you want to generate them for debugging purposes.
- `javadoc`: tells Yokedox which generator to use - or in this case, tells Yokedox which generator was used to generate the result at `debugGeneratorResultPath`

>Remember to rebuild Yokedox whenever you made a change to it.

THIS IS A TEST PLS IGNORE
