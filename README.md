# maven-docs

#### What is POM packaging in maven and what is purpose of parent pom?

```
<packaging>pom</packaging>
```
- `pom` is basically a container of submodules, each submodule is represented by a subdirectory in the same directory as `pom.xml` with `pom` packaging.
-  It is also used to structure the project to avoid redundancies or duplicate configurations using inheritance between pom files. It helps in easy maintenance in long term.

   A parent POM can be declared with packaging pom. It is not meant to be distributed because it is only referenced from other projects.
   
   
   Maven parent pom can contain almost everything and those can be inherited into child pom files e.g

   - Common data – Developers’ names, SCM address, distribution management etc.
   - Constants – Such as version numbers
   - Common dependencies – Common to all child. It has same effect as writing them several times in individual pom files.
   - Properties – For example plugins, declarations, executions and IDs.
   - Configurations
   - Resources
