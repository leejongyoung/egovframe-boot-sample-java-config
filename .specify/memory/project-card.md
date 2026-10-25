# egovframe-boot-sample-java-config: project context

## Role, scope, and public entry points

`README.md` describes a Spring Boot simple-board reference application using Java configuration
and KRDS UI. `src/main/java/egovframework/example/sample/` exposes the sample controller,
service interface, mapper, and value objects; `example/config/` wires data access, transactions,
properties, and other services. `Docs/java-config-convert.md` documents configuration conversion;
`script/ddl/` contains database-specific sample schemas. Preserve board CRUD, pagination,
validation, view/controller behavior, mapper contracts, and configuration compatibility.

## Build and verification evidence

- `pom.xml` packages a JAR, inheriting `org.egovframe.boot:egovframe-boot-starter-parent:5.0.1`.
  Dependencies include eGovFrame runtime modules and HSQLDB; repositories include Maven Central
  and the eGovFrame repository. README specifies JDK 17 / Boot 3.5.6 / Spring 6.2.11.
- `.github/workflows/maven.yml` targets `main` push/PR, uses JDK 17, and runs
  `mvn -B package --file pom.xml`. There is no observed workflow targeting `work`.
  Read the POM/inherited test configuration and affected tests before claiming discovered coverage.
- README documents `mvn spring-boot:run`, IDE Spring Boot App startup, and default port 8080
  configured through `src/main/resources/application.properties`.
- `src/test/java/egovframework/example/` contains value-object, service, mapper, controller,
  pagination, and Selenium-named test sources. Their existence does not establish execution;
  browser-dependent checks need a suitable browser/driver and test discovery configuration.
  Runtime checks require suitable datasource configuration and schema, and dependency access.

## Contribution and submission baseline

Actual parent: `eGovFramework/egovframe-boot-sample-java-config`. No repository-local AGENTS
or contribution guide was found in the root/file inventory. Follow the fork constitution without
claiming upstream process requirements that were not documented. Fetch the actual upstream
default branch and record its SHA, preserving existing submission branches and PRs.
Prepare `upstream-submit` directly from that SHA; use a separate submission worktree for later
application fixes. Keep adoption artifacts and their commit on `work`; adoption creates no PR.

## Exploration limits

No `.codegraph/` index was present. Context is based on targeted README, POM, CI, and source/test
path inspection. No application test/build or runtime launch was performed.


## Maintenance process

Follow [constitution.md](constitution.md) for the domain-card, assessment, planning, verification,
and submission gates. Commands are installed under `.omp/commands/`; read them as agent
instructions. No application build or test was run for tool adoption. Scaffold checks establish
tool installation only, not application correctness.
