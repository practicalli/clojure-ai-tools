# Clojure Setup

[Practicalli Clojure includes a complete description of a Clojure setup](https://practical.li/clojure/install/){target=_blank}, which installs:

- Java Virtual Machine
- Clojure CLI
- Practicalli Clojure CLI Config


## Clojure MCP

https://github.com/bhauman/clojure-mcp and/or https://github.com/bhauman/clojure-mcp-light


### Install ClojureMCP

Use an alias (something like this?)

```clojure
  :ai/clojure-mcp
  {:replace-deps {io.github.bhauman/clojure-mcp
                  {:git/tag "v0.5.1" :git/sha "c9cdd6b"}}
   :exec-fn clojure-mcp.main/start}
```

TODO: add ai/clojure-mcp alias to Practicalli Clojure CLI Config

Install as a tool

clojure -Ttools install-latest

```shell
clojure -Ttools install-latest :lib io.github.bhauman/clojure-mcp :as mcp
```


### CLI tools

Install ripgrep


### Register it as an MCP server in your LLM client.



## Additional tools

!!! INFO "Clojure connected editor"
    A [Clojure connected editor](/clojure/clojure-editors/) provides the most effective way to write and maintain Clojure projects.  The editor connects to (or starts) a Clojure REPL and code can be evaluated as its typed, showing the results instantly in line with the code.

    [Clojure LSP server](/clojure/clojure-editors/clojure-lsp/) generates static analysis of code which editors can surface as code diagnostics.  Analysis supports effective code navigate and refactor tools. [:fontawesome-solid-book-open: Practicalli Clojure LSP config](/clojure/clojure-editors/clojure-lsp/) configures

!!! INFO "Data Inspectors"
    [Data inspectors](/clojure/data-inspectors/) visualize results of Clojure code evaluation and allow navigation of nested data or paging through large data sets.

    [Portal](/clojure/data-inspector/portal/) is highly recommended data inspector and included in projects generated with [Practicalli Project Templates](/clojure/clojure-cli/projects/templates/practicalli/).


??? INFO "Alternative development tools"
    [Leiningen](https://leiningen.org){target=_blank} is the long-standing development tool for Clojure.  All the code examples in this book should work with Leiningen when a correctly configured `project.clj` file is created which includes all the necessary library dependencies.  Libraries included via aliases should be added as either `:dev-dependencies` or `:aliases` in the Leiningen `project.clj` file.
