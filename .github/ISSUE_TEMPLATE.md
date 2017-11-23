<!-- For general purpose questions, use Stack Overflow http://stackoverflow.com/questions/tagged/hyperledger -->

## Description
<!-- Describe your issue or user story in detail -->
I build the example, then throw exception, Example is not override superclass ChaincodeBase.init() and invoke()

## Describe How to Reproduce
<!-- If an issue, provide sufficient context and steps to reproduce the issue -->

cd $gopath/src/github.com/hyperledger/fabric/examples/chaincode/java/Example
gradle -b build.gradle build
:examples:chaincode:java:Example:compileJava

$gopath/src/github.com/hyperledger/fabric/examples/chaincode/java/Example/src/main/java/example/Example.java:66: error: Example is not abstract class, does not implements ChaincodeBase's abstract methond invoke(ChaincodeStub)
public class Example extends ChaincodeBase {
       ^
java\Example\src\main\java\example\Example.java:75: error: String cann't convert to byte[]
                                stub.putState(args[i], args[i + 1]);
                                                           ^
