# sbt-isabelle-component
MWE for an `sbt` setup of an external Isabelle component.

## How to use
1. Setup Isabelle:
   - Checkout: `git submodule init && git submodule update`
   - Build isabelle:
     - `./isabelle/bin/isabelle components -I`
     - `./isabelle/bin/isabelle components -a`
     - `./isabelle/bin/isabelle jedit -bf`
2. Configure Isabelle to use our component:
   - Add component to your Isabelle user settings:
     ```
     echo "init_component \\"$(pwd)/my-component/scala-2.12\\"" >> ~/.isabelle/etc/settings
     ```
3. Run via tool: `./sbt "project my-component" run`
