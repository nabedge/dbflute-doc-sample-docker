FROM openjdk:8u162

RUN git clone https://github.com/nabedge/dbflute-doc-sample.git

RUN cd dbflute-doc-sample && sh ./mvnw clean

CMD \
    cd dbflute-doc-sample \
    && sh ./mvnw clean compile \
    && sh ./target/dbflute_dfclient/manage.sh 21,22 \
    && cp -R ./target/* /target-on-container

