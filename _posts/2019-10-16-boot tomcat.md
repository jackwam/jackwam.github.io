# Spring boot 외부 톰캣 사용 방법
1.  @SpringBootApplication 파일에 추가
public class xxxApplication <b>extends SpringBootServletInittializer</b>{
  <b>
  @Override
  protected SpringApplicationBuilder configure(SpringApplicationBuilder application){
   return application.sources(xxxApplication.class);
  }
  </b>
  
  public static void main(String[] args){
    SpringApplication.run(xxx.Application.class, args);
  }
}

2. pom.xml 설정추가 - tomcat 미사용 설정
<b>
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-tomcat</artifactId>
  <scope>provided</scope>
</dependency>
</b>

3. application.properties port설정 주석
<b> #server.port = 18081</b>

$ tomcat security오류일 경우 enable security 설정 


