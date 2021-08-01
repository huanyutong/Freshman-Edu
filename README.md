# Freshman-Edu
1、创建基础工程
1.1 工程结构
CMS及其它服务端工程基于maven进行构建，首先需要创建如下基础工程：
1）empty工程（空项目）		：Freshman-Edu			作为本项目的工作空间		路径：\Freshman-Edu
2）parent工程（父工程）		：edu-framework-parent	提供依赖管理				路径：\Freshman-Edu\edu-framework-parent
3）common工程（通用工程）		：edu-framework-common	提供各层封装				路径：\Freshman-Edu\edu-framework-common		父工程：edu-framework-parent
4）model工程（模型工程）		：edu-framework-model	提供统一的模型类管理		路径：\Freshman-Edu\edu-framework-model		父工程：edu-framework-parent
5）utils工程（工具类工程）	：edu-framework-utils	提供本项目所使用的工具类	路径：\Freshman-Edu\edu-framework-utils		父工程：edu-framework-parent
6）Api工程（接口工程）		：edu-service-api		统一管理本项目的服务接口	路径：\Freshman-Edu\edu-service-api			父工程：edu-framework-parent

统一groupid：com.freshman
统一包名：groupid+项目名称

依赖关系
edu-framework-model 依赖于 common工程（通用工程）、utils工程（工具类工程）
edu-service-api 依赖于 common工程（通用工程）、model工程（模型工程）

依赖包
ch.qos.logback					:logback-classic					:1.2.4
ch.qos.logback					:logback-core						:1.2.4
com.alibaba						:fastjson							:1.2.76
com.fasterxml					:classmate							:1.5.1
com.fasterxml.jackson.core		:jackson-annotations				:2.12.4
com.fasterxml.jackson.core		:jackson-core						:2.12.4
com.fasterxml.jackson.core		:jackson-databind					:2.12.4
com.fasterxml.jackson.datatype	:jackson-datatype-jdk8				:2.12.4
com.fasterxml.jackson.datatype	:jackson-datatype-jsr310			:2.12.4
com.fasterxml.jackson.module	:jackson-module-parameter-names		:2.12.4
com.google.code.findbugs		:jsr305								:3.0.2
com.google.errorprone			:error_prone_annotations			:2.5.1
com.google.guava				:failureaccess						:1.0.1
com.google.guava				:guava								:30.1.1-jre
com.google.guava				:listenablefuture					:9999.0-empty-to-conflict-with-guava
com.google.j2objc				:j2objc-annotations					:1.3
com.ibm.icu						:icu4j								:61.1
com.jayway.jsonpath				:json-path							:2.5.0
com.sun.activation				:jakarta.activation					:1.2.2
com.sun.istack					:istack-commons-runtime				:3.0.12
com.vaadin.external.google		:android-json						:0.0.20131108.vaadin1
commons-code					:commons-codec						:1.5
commons-fileupload				:commons-fileuplad					:1.4
commons-logging					:commons-logging					:1.2
commons-io						:commons-io							:2.2->20030203.000550
io.github.classgraph			:classgraph							:4.8.83
io.github.openfeign.form		:feign-form							:3.8.0
io.github.openfeign.form		:feign-form-spring					:3.8.0
io.github.openfeign.form		:feign-core							:10.12
io.github.openfeign.form		:feign-slf4j						:10.12
io.springbox					:springfox-core						:3.0.0
io.springbox					:springfox-schema					:3.0.0
io.springbox					:springfox-spi						:3.0.0
io.springbox					:springfox-spring-web				:3.0.0
io.springbox					:springfox-spring-webflux			:3.0.0
io.springbox					:springfox-spring-webmvc			:3.0.0
io.springbox					:springfox-swagger2					:3.0.0
io.springbox					:springfox-swagger-common			:3.0.0
io.springbox					:springfox-swagger-ui				:3.0.0
io.swagger.core.v3				:swagger-annotations				:2.1.2
io.swagger						:swagger-annotations				:1.5.20
io.swagger						:swagger-models						:1.5.20
javax.activation				:javax.activation-api				:1.2.0->1.2.2
jakarta.annotation				:jakarta.annotation-api				:1.3.5
jakarta.xml.bind				:jakarta.xml.bind-api				:2.3.3
javax.persistence				:javax.persistence-api				:2.2
javax.servlet					:javax.servlet-api					:4.0.1
javax.xml.bind					:jaxb-api							:2.3.1
net.bytebuddy					:byte-buddy							:1.10.22
net.bytebuddy					:byte-buddy-agent					:1.10.22
net.minidev						:accessors-smart					:2.4.7
net.minidev						:json-smart							:2.4.7
net.lingala.zip4j				:zip4j								:2.9.0
org.abego.treelayout			:org.abego.treelayout.core			:1.0.3
org.antlr						:antlr4								:4.9.1
org.antlr						:antlr4-runtime						:4.9.1
org.antlr						:antlr-runtime						:4.9.1
org.antlr						:ST4								:4.3
org.apache.commons				:commons-lang3						:3.12.0
org.apache.httpcomponents		:httpclient							:4.5.13
org.apache.httpcomponents		:httpcore							:4.4.14
org.apache.logging.log4j		:log4j-api							:2.14.1
org.apache.logging.log4j		:log4j-to-slf4j						:2.14.1
org.apache.tomcat.embed			:tomcat-embed-core					:9.0.50
org.apache.tomcat.embed			:tomcat-embed-el					:9.0.50
org.apache.tomcat.embed			:tomcat-embed-websocket				:9.0.50
org.apiguardian					:apiguardian-api					:1.1.0
org.aspectj						:aspectjweaver						:1.9.7
org.assertj						:assertj-core						:3.19.0
org.bouncycastle				:bcpkix-jdk15on						:1.68
org.bouncycastle				:bcppro-jdk15on						:1.68
org.checkframework				:checker-qual						:3.8.0
org.glassfish.jaxb				:jaxb-runtime						:2.3.4
org.glassfish.jaxb				:txw2								:2.3.4
org.glassfish.jaxb				:javax.json							:1.0.4
org.hamcrest					:hamcrest							:2.2
org.hibernate.common			:hibernate-commons-annotations		:5.1.2.Final
org.hibernate.orm				:hibernate-core						:6.0.0.Alpha8
org.jboss.logging				:jboss-logging						:3.4.2.Final
org.jboss.spec.javax.transaction:jboss-transaction-api_1.2_spec		:1.1.1.Final
org.jboss						:jandex								:2.2.3.Final
org.junit.jupiter				:junit-jupiter						:5.7.2
org.junit.jupiter				:junit-jupiter-api					:5.7.2
org.junit.jupiter				:junit-jupiter-engine				:5.7.2
org.junit.jupiter				:junit-jupiter-params				:5.7.2
org.junit.platform				:junit-platform-commons				:1.7.2
org.junit.platform				:junit-platform-engine				:1.7.2
org.mapstruct					:mapstruct							:1.3.1.Final
org.mockito						:mockito-core						:3.9.0
org.mockito						:mockito-junit-jupiter				:3.9.0
org.mongodb						:bson								:4.3.0
org.mongodb						:mongodb-driver-core				:4.3.0
org.mongodb						:mongodb-driver-sync				:4.3.0
org.objenesis					:objenesis							:3.2
org.opentest4j					:opentest4j							:1.2.0
org.ow2.asm						:asm								:9.1
org.projectlombok				:lombok								:1.18.20
org.skyscreamer					:jsonassert							:1.5.0
org.slf4j						:jul-to-slf4j						:1.7.32->2.0.0-alpha2
org.slf4j						:slf4j-api							:1.7.32->2.0.0-alpha2
org.slf4j						:slf4j-log4j12						:1.7.32->2.0.0-alpha2
org.springframework				:spring-aop							:5.3.9
#org.springframework				:spring-beans						:5.3.9
org.springframework				:spring-context						:5.3.9
#org.springframework				:spring-core						:5.3.9
org.springframework				:spring-expression					:5.3.9 由spring-boot/spring-boot-autoconfigure共同引入
#org.springframework				:spring-jcl							:5.3.9
org.springframework				:spring-test						:5.3.9
org.springframework				:spring-tx							:5.3.9
##org.springframework				:spring-web							:5.3.9 含aop/beans/core/jcl
org.springframework.boot		:spring-boot						:2.5.3
org.springframework.boot		:spring-boot-autoconfigure			:2.5.3
org.springframework.boot		:spring-boot-starter				:2.5.3
org.springframework.boot		:spring-boot-starter-aop			:2.5.3
org.springframework.boot		:spring-boot-starter-data-mongodb	:2.5.3
org.springframework.boot		:spring-boot-starter-json			:2.5.3
org.springframework.boot		:spring-boot-starter-logging		:2.5.3
org.springframework.boot		:spring-boot-starter-test			:2.5.3
org.springframework.boot		:spring-boot-starter-tomcat			:2.5.3
org.springframework.boot		:spring-boot-starter-web			:2.5.3
org.springframework.boot		:spring-boot-test					:2.5.3
org.springframework.boot		:spring-boot-test-autoconfigure		:2.5.3
org.springframework.boot		:spring-aop							:5.3.9
org.springframework.boot		:spring-beans						:5.3.9
org.springframework.boot		:spring-context						:5.3.9
org.springframework.boot		:spring-core						:5.3.9
org.springframework.boot		:spring-expression					:5.3.9
org.springframework.boot		:spring-jcl							:5.3.9
org.springframework.boot		:spring-web							:5.3.9
org.springframework.boot		:spring-webmvc						:5.3.9
org.springframework.cloud		:spring-cloud-commons				:3.0.3
org.springframework.cloud		:spring-cloud-context				:3.0.3
org.springframework.cloud		:spring-cloud-openfeign-core		:3.0.3
org.springframework.cloud		:spring-cloud-starter				:3.0.3
org.springframework.cloud		:spring-cloud-starter-openfeign		:3.0.3
org.springframework.data		:spring-data-commons				:2.5.3
org.springframework.data		:spring-data-mongodb				:3.2.3
org.springframework.security	:spring-security-crypto				:5.5.1
org.springframework.security	:spring-security-jwt				:1.1.1.RELEASE
org.springframework.security	:spring-security-rsa				:1.0.10.RELEASE
org.springframework.plugin		:spring-plugin-core					:2.0.0.RELEASE
org.springframework.plugin		:spring-plugin-metadata				:2.0.0.RELEASE
org.xmlunit						:xmlunit-core						:2.8.2
org.yaml						:snakeyaml							:1.28

7）CMS服务工程（页面查询服务）	：edu-service-manage-cms	
本项目作为一个大型的在线教育平台，对CMS系统的定位是对各各网站（子站点）页面的管理，主要管理由于运营需要而经常变动的页面，从而实现根据运营需要快速进行页面开发、上线的需求