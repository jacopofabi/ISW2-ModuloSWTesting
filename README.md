# Report ISW2: Modulo Software Testing

## JCS  [![Build Status](https://travis-ci.com/jacopofabi/JCS-ISW2.svg?branch=main)](https://travis-ci.com/jacopofabi/JCS-ISW2)
  https://github.com/jacopofabi/JCS-ISW2  
  
Esecuzione dei test e analisi coverage tramite JaCoCo:
```bash
mvn clean verify -DjarfatPath=../src/test/lib/jcs-1.3-fat.jar

./JCS-ISW2/jacocoLibSnippets.sh 
```
I report saranno generati in ```..\JCS-ISW2\target\jacoco-gen\jcs-coverage```

# BookKeeper  [![Build Status](https://travis-ci.com/jacopofabi/bookkeeper.svg?branch=master)](https://travis-ci.com/jacopofabi/bookkeeper) [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=jacopofabi_bookkeeper&metric=coverage)](https://sonarcloud.io/dashboard?id=jacopofabi_bookkeeper)
  https://github.com/jacopofabi/bookkeeper
  
Esecuzione dei test e analisi coverage tramite JaCoCo:
```bash
mvn clean verify
```
Esecuzione framework PIT:
```bash
mvn clean verify -P pit-test
```
I report della fase di mutation testing saranno generati in ```..\bookkeeper-server\target\pit-reports```


# Avro [![Build Status](https://travis-ci.com/jacopofabi/avro.svg?branch=master)](https://travis-ci.com/jacopofabi/avro)  [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=jacopofabi_avro&metric=coverage)](https://sonarcloud.io/dashboard?id=jacopofabi_avro)
  https://github.com/jacopofabi/avro
  
Esecuzione dei test e analisi coverage tramite JaCoCo:
```bash
mvn "-Dtest=org/apache/avro/mytests/*Test" -DfailIfNoTests=false clean verify -Dcoverage=true
```
Esecuzione framework PIT:
```bash
mvn "-Dtest=org/apache/avro/mytests/*Test" -DfailIfNoTests=false clean verify -Dcoverage=true -Dmutation=true
```
I report della fase di mutation testing saranno generati in ```..\avro-child\target\pit-reports```