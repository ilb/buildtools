# buildtools

checkstyle, pmd settings, originally from apache cxf project

## Changelog

### buildtools-1.0

1. originally coped from  from cxf.build-utils-3.4.4
2. disabled ImportOrder check (Netbeans configuration required to automate import order)
see https://stackoverflow.com/questions/21024956/how-to-configure-organizing-of-java-imports-in-netbeans
3. disabled Licensed check (Apache license header)
4. exclude org.junit.Assert,javax.xml.bind.annotation,org.junit.jupiter.api.Assertions packages from AvoidStarImport to address tests and jeddict models
5. temporarily disable HiddenField module. not working with "withSomething" chain methods, even with setterCanReturnItsClass.
see https://groups.google.com/g/checkstyle-devel/c/aPNYF3RC_yU?pli=1
6. extend LineLength to max of 250 characters instead of 120
7. disable caseIndent=0 (overrides netbeans default)
8. exclude TooFewBranchesForASwitchStatement
9. max ParameterNumber limit set to 10
10. disable InterfaceIsType (interface could extend base and change only type params)
11. disable MissingSwitchDefault