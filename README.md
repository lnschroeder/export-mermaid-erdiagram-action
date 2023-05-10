# export-mermaid-erdiagram-action
This is a GitHub Action to export an entity relationship diagram as SVG, PNG, or PDF from a database.
- [Mermerd](https://github.com/KarnerTh/mermerd) is used to generate a [MermaidJS](https://mermaid.js.org/) entity relationship diagram as `.mmd` file.
- [mermaid-cli](https://github.com/mermaid-js/mermaid-cli) is used to convert the `.mmd` into a printable file format.

## Usage
- create a Mermerd config `.yml`
- add a step to your workflow job
  ```yml
  - name: Generate Mermaid ER diagram
    uses: lnschroeder/export-mermaid-erdiagram-action@v1.0.0
    with:
      config: mermerdConfig.yaml
      output: output.svg
      connectionString: driver://user:password@host:port/database
  ```
- see [action.yml](action.yml) for more information
