<!--
**lcqff/lcqff** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->




<div align="center">

<!-- 타이핑 타이틀 -->
[![Typing SVG](https://readme-typing-svg.demolab.com?font=Mingzat&weight=500&size=30&duration=7000&pause=4000&color=000000&center=true&vCenter=true&repeat=true&width=1035&lines=%E2%AC%87+Don't+Feed+My+Goose+(It's+Fat)+%E2%AC%87)](https://git.io/typing-svg)

<!--스프링 거위(먹이금지)-->
<a href="https://github.com/devxb/gitanimals"> <img src="https://render.gitanimals.org/lines/lcqff?pet-id=937" width="1000" height="100"/></a>
안녕하세요 <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="20px" height="20px"/> 제 Github에 온 걸 환영해요. <br> 제가 공부하는 내용들이 궁금하시다면 아래 두 레파지토리에 놀러오세요.

  <a href="https://github.com/lcqff/Yeonnu-Java-lab" target="_blank">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=lcqff&repo=Yeonnu-Java-lab&theme=dracula&theme=transparent"/>
  </a>
  <a href="https://github.com/lcqff/Yeonnu-Infra-lab" target="_blank">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=lcqff&repo=Yeonnu-Infra-lab&theme=dracula&theme=transparent" />
  </a>


##

### 🔧 Technologies & Tools
![spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![mysql](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
  
### 📚 Currently Studying...
![spring security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=Spring-Security&logoColor=white)
![docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![aws](https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)

<br>

## ✍ Blog & Writing
공부한 내용들을 까먹지 않기 위해 블로그를 작성하고 있어요. <br> 제가 공부하는 방법과, 문제를 해결하는 방법이 궁금하시다면 놀러오세요.

<!-- BLOG-POST-LIST:START -->
 ✨ [Spring Security&lpar;1&rpar;- OAuth2 구글 로그인 구현](https://lcqff.github.io/spring-security1/) | 👀 &lt;hr /&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h1 id=&quot;개요&quot;&gt;개요&lt;/h1&gt;

&lt;p&gt;&lt;a href=&quot;https://lcqff.github.io/kakao-login/&quot;&gt;수동 인증 처리를 통한 Oauth2 로그인&lt;/a&gt;을 직접 구현해본적 있으나, 이러한 방식은 인증과 인가 방식에서 여러가지 불편함이 있었다.&lt;/p&gt;

&lt;p&gt;해당 방식은 직접 인가코드를 호출하고, 토큰을 요청하고, 사용자 정보를 요청하는 번거로운 과정을 백엔드와 프론트상에서 수동으로 처리해야 했다. 
또한 인가 처리가 아름답지 못하여 권한 처리를 할때마다 ‘내가 Spring Security를 알았으면!’하고 탄식했다.&lt;/p&gt;

&lt;p&gt;인증과 인가는 대부분의 어플리케이션에서의 필수 요소이기 때문에, 백엔드 개발자라면 Spring Security를 배워두는것이 좋겠다는 생각이 들었다.&lt;/p&gt;

&lt;p&gt;이번 게시글에서 다룰 내용은 아래와 같다.&lt;/p&gt;
&lt;blockquote&gt;
  &lt;p&gt;구글 콘솔에서 프로젝트를 생성하는 방법을 알아본다.
Spring Security를 사용한 Configuration 흐름을 알아본다.&lt;br /&gt;
Spring Security를 사용한 인증 처리 흐름을 알아본다.&lt;br /&gt;
Spring Security를 사용하여 실제 구글 Oauth2 로그인을 구현한다.&lt;br /&gt;
여러 Oauth2 서비스가 동일한 코드를 사용할 수 있는 인터페이스를 구현한다.&lt;/p&gt;
&lt;/blockquote&gt;

&lt;p&gt;JWT 토큰 생성과 인가 처리와 같은 부분은 다른 포스팅으로 다룰 예정이다.&lt;/p&gt;

&lt;hr /&gt;

&lt;h1 id=&quot;google-새-프로젝트-생성&quot;&gt;&lpar;Google&rpar; 새 프로젝트 생성&lt;/h1&gt;

&lt;p&gt;&lt;a href=&quot;https://console.cloud.google.com/&quot;&gt;https://console.cloud.google.com&lt;/a&gt;에 접속하여 새로운 프로젝트를 생성하자.&lt;br /&gt;
새 프로젝트를 생성한 뒤 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;clientId&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;secret&lt;/code&gt;을 받아와야 한다.&lt;/p&gt;

&lt;h2 id=&quot;oauth-동의화면&quot;&gt;OAuth 동의화면&lt;/h2&gt;

&lt;p&gt;OAuth 동의화면에서 Scope설정을 할 수 있다.&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/c0b30a35-2424-4c77-b8d3-d3f02d44cd4e&quot; alt=&quot;image&quot; /&gt;
앱 정보는 필수항목만 작성한다.&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/1c6cf04b-1f80-4263-860d-2e252fa07e83&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;위 두가지 항목만 요청한다.&lt;br /&gt;
open Id같은 경우 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OpenID Connect&lt;/code&gt;를 사용하기 위해서 필요한데, 나는 OIDC를 사용하지 않을거다&lt;/p&gt;

&lt;p&gt;&lpar;OIDC는 이후에 학습해봐야겠다…&rpar;&lt;/p&gt;

&lt;h2 id=&quot;사용자-인증-정보&quot;&gt;사용자 인증 정보&lt;/h2&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/3b3f8593-3a4c-4ba6-b24e-5eec6d3de6dd&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;리다이렉션 URI는  Oauth2 요청을 보낼  백엔드 주소&lpar;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;~/login/oauth2/code/{소셜 서비스 명}&lt;/code&gt;&rpar;로 한다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;blockquote&gt;
  &lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;/login/oauth2/code/{소셜 서비스 명}&lt;/code&gt; 은 &lt;strong&gt;Spring Security에서 기본적으로 제공해주는 리다이렉션Url&lt;/strong&gt;로, 다른 설정을 하지 않는다면 해당 엔드포인트를 로그인 요청으로 사용한다.&lt;/p&gt;

  &lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/ca223473-3421-4f22-8431-d056a8d42fd1&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;
  &lt;cap&gt;Oauth2LoginAuthenticationFilter에 기본 설정되어있다.&lt;/cap&gt;
  &lt;p&gt;&lt;br /&gt;&lt;/p&gt;

  &lt;p&gt;위 redirection url에 의해 로그인이 성공하는 경우 백엔드 서버로 리다이렉션돼 토큰 발급 및 사용자 정보 요청이 진행되게 된다.&lt;/p&gt;

  &lt;p&gt;&lpar;프론트 주소로 리다이렉션할 경우 토큰 발급과 사용자 정보 요청이 불가능해짐으로 &lt;strong&gt;항상 백엔드로 redirection 되게 하자&lt;/strong&gt;.&rpar;&lt;/p&gt;
&lt;/blockquote&gt;

&lt;p&gt;Oauth2 로그인을 위해선 사용자 인증 정보 설정이 끝나고 발급받는 클라이언트 ID와 클라이언트 보안 비밀번호&lpar;Secret&rpar;가 필요하다.&lt;/p&gt;

&lt;h1 id=&quot;설정파일-작성&quot;&gt;설정파일 작성&lt;/h1&gt;

&lt;div class=&quot;language-yaml highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;na&quot;&gt;spring&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;:&lt;/span&gt;
  &lt;span class=&quot;na&quot;&gt;security&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;:&lt;/span&gt;
    &lt;span class=&quot;na&quot;&gt;oauth2&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;:&lt;/span&gt;
      &lt;span class=&quot;na&quot;&gt;client&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;:&lt;/span&gt;
        &lt;span class=&quot;na&quot;&gt;registration&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;:&lt;/span&gt;
          &lt;span class=&quot;na&quot;&gt;google&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;:&lt;/span&gt;
            &lt;span class=&quot;na&quot;&gt;client-id&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;:&lt;/span&gt; &lt;span class=&quot;pi&quot;&gt;{&lt;/span&gt;&lt;span class=&quot;nv&quot;&gt;클라이언트 ID&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;}&lt;/span&gt;
            &lt;span class=&quot;na&quot;&gt;client-secret&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;:&lt;/span&gt; &lt;span class=&quot;pi&quot;&gt;{&lt;/span&gt;&lt;span class=&quot;nv&quot;&gt;클라이언트 보안 비밀번호&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;}&lt;/span&gt;
            &lt;span class=&quot;na&quot;&gt;scope&lt;/span&gt;&lt;span class=&quot;pi&quot;&gt;:&lt;/span&gt; &lt;span class=&quot;s&quot;&gt;profile, email&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;사용자 인증 정보에서 가져온 클라이언트 ID와 클라이언트 보안 비밀번호를 yml 파일에 입력해준다. &lt;br /&gt;
민감 정보이기 때문에 외부에 노출되지 않도록 한다.&lt;/p&gt;

&lt;p&gt;naver나 kakao의 설정파일 같은 경우 &lt;a href=&quot;https://lcqff.github.io/kakao-login/&quot;&gt;&lt;strong&gt;다른 포스팅&lt;/strong&gt;&lt;/a&gt;을 참고하자.&lt;/p&gt;

&lt;h1 id=&quot;spring-security-configuration-처리흐름&quot;&gt;Spring Security Configuration 처리흐름&lt;/h1&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/2e751f02-4cc8-4429-b2bd-c2e0b5d08820&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;Spring Security의 설정과 초기화는 &lt;strong&gt;SecurityConfigurer&lt;/strong&gt;의 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;init&lpar;&rpar;&lt;/code&gt;과 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;configure&lpar;&rpar;&lt;/code&gt;에서 일어난다.&lt;/p&gt;

&lt;p&gt;위 두 메서드는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;HttpSecurity&lt;/code&gt;의 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;oauth2Login&lpar;&rpar;&lt;/code&gt; 메서드에 의해 실행되는데, oauth2Login&lpar;&rpar;은 일반적으로 개발자가 직접 &lt;strong&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;SecurityConfiguration&lt;/code&gt;&lt;/strong&gt;과 같은 설정 클래스를 작성하는 것으로 실행된다.&lt;/p&gt;

&lt;h2 id=&quot;init&quot;&gt;init&lpar;&rpar;&lt;/h2&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;
	&lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;init&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;no&quot;&gt;B&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;http&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;throws&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Exception&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	
		&lt;span class=&quot;c1&quot;&gt;// 인가코드 리다이렉션을 인터셉트하여 Access Token 및 사용자 정보를 요청하는 필더 OAuth2LoginAuthenticationFilter&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;OAuth2LoginAuthenticationFilter&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;authenticationFilter&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2LoginAuthenticationFilter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;...&rpar;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;setAuthenticationFilter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;authenticationFilter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		
		&lt;span class=&quot;c1&quot;&gt;// this.loginProcessingUrl = DEFAULT_FILTER_PROCESSES_URI = &quot;/login/oauth2/code/*&quot;&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// 인가 코드 요청이 Redirection되고, OAuth2LoginAuthenticationFilter가 인터셉트할 주소를 DEFAULT_FILTER_PROCESSES_URI로 설정한다.&lt;/span&gt;
		&lt;span class=&quot;kd&quot;&gt;super&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;loginProcessingUrl&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;loginProcessingUrl&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt; 

	 	&lt;span class=&quot;o&quot;&gt;....&lt;/span&gt;
		
		&lt;span class=&quot;c1&quot;&gt;// 엑세스 토큰 교환용&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;OAuth2AccessTokenResponseClient&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;lt;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;OAuth2AuthorizationCodeGrantRequest&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;gt;&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;accessTokenResponseClient&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;getAccessTokenResponseClient&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// 실제 사용자 정보 요청 처리용&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;OAuth2UserService&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;lt;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;OAuth2UserRequest&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;gt;&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oauth2UserService&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;getOAuth2UserService&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		
		&lt;span class=&quot;c1&quot;&gt;// 실질적인 인증 처리용 &lpar;엑세스 토큰 요청, 사용자 정보 요청&rpar;&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;OAuth2LoginAuthenticationProvider&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oauth2LoginAuthenticationProvider&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2LoginAuthenticationProvider&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;
				&lt;span class=&quot;n&quot;&gt;accessTokenResponseClient&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oauth2UserService&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	
		 &lt;span class=&quot;o&quot;&gt;....&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;init&lpar;&rpar;&lt;/code&gt;에서는 Spring Security에서 사용되는 인스턴스들을 초기화한다.&lt;/p&gt;

&lt;p&gt;대표적으로 초기화 되는 인스턴스들은 아래와 같다.&lt;/p&gt;

&lt;ul&gt;
  &lt;li&gt;&lt;strong&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationFilter&lt;/code&gt;&lt;/strong&gt;: 리다이렉션된 인가코드를 사용하여 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationProvider&lt;/code&gt;을 통해 Access Token을 요청하고 사용자 정보를 요청하는 전반적인 인증과정을 담당한다.&lt;/li&gt;
  &lt;li&gt;&lt;strong&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationProvider&lt;/code&gt;&lt;/strong&gt;: accessToken을 요청하고 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2UserService&lt;/code&gt;에 사용자 정보를 요청하여 OAuth2LoginAuthenticationFilter에 반환한다.&lt;/li&gt;
  &lt;li&gt;&lt;strong&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2UserService&lt;/code&gt;&lt;/strong&gt;: 사용자 정보을 제공한다.&lt;/li&gt;
&lt;/ul&gt;

&lt;h2 id=&quot;configure&quot;&gt;configure&lpar;&rpar;&lt;/h2&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;configure&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;no&quot;&gt;B&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;http&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;throws&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Exception&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	
		&lt;span class=&quot;c1&quot;&gt;// OAuth2AuthorizationRequestRedirectFilter 초기화&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;OAuth2AuthorizationRequestRedirectFilter&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;authorizationRequestFilter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationEndpointConfig&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationRequestResolver&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;!=&lt;/span&gt; &lt;span class=&quot;kc&quot;&gt;null&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;authorizationRequestFilter&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2AuthorizationRequestRedirectFilter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;
					&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationEndpointConfig&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationRequestResolver&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;else&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		
		 &lt;span class=&quot;c1&quot;&gt;// 인가코드의 발급 요청을 보내고, OAuth2AuthorizationRequestRedirectFilter가 인터셉트할 주소를 설정한다.&lt;/span&gt;
		 &lt;span class=&quot;c1&quot;&gt;// 기본 주소: /oauth2/authorization/*&lt;/span&gt;
			&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;authorizationRequestBaseUri&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationEndpointConfig&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationRequestBaseUri&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
			&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;authorizationRequestBaseUri&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;==&lt;/span&gt; &lt;span class=&quot;kc&quot;&gt;null&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
				&lt;span class=&quot;n&quot;&gt;authorizationRequestBaseUri&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2AuthorizationRequestRedirectFilter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;DEFAULT_AUTHORIZATION_REQUEST_BASE_URI&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
			&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
			
			&lt;span class=&quot;c1&quot;&gt;//커스터마이즈된 URI가 존재하는 경우 해당 URI를 사용한다.&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;authorizationRequestFilter&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2AuthorizationRequestRedirectFilter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;
					&lt;span class=&quot;nc&quot;&gt;OAuth2ClientConfigurerUtils&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getClientRegistrationRepository&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getBuilder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;,&lt;/span&gt;
					&lt;span class=&quot;n&quot;&gt;authorizationRequestBaseUri&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	    &lt;span class=&quot;o&quot;&gt;....&lt;/span&gt;
		
		&lt;span class=&quot;c1&quot;&gt;// 인가 코드 요청이 Redirection되고, OAuth2LoginAuthenticationFilter가 인터셉트할 주소를 커스터마이즈 할 수 있다. &lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// init&lpar;&rpar;에서 기본 url인 DEFAULT_FILTER_PROCESSES_URI로 설정되어 있다.&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// 기본 주소: /login/oauth2/code/*&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;OAuth2LoginAuthenticationFilter&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;authenticationFilter&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getAuthenticationFilter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;redirectionEndpointConfig&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationResponseBaseUri&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;!=&lt;/span&gt; &lt;span class=&quot;kc&quot;&gt;null&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;authenticationFilter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;setFilterProcessesUrl&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;redirectionEndpointConfig&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationResponseBaseUri&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationEndpointConfig&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationRequestRepository&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;!=&lt;/span&gt; &lt;span class=&quot;kc&quot;&gt;null&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;authenticationFilter&lt;/span&gt;
				&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;setAuthorizationRequestRepository&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationEndpointConfig&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizationRequestRepository&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

		&lt;span class=&quot;o&quot;&gt;....&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;configure&lpar;&rpar;&lt;/code&gt;에서는 인가코드 발급을 처리하는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2AuthorizationRequestRedirectFilter&lt;/code&gt;와  엑세스 토큰 요청 및 사용자 정보를 교환하는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationFilter&lt;/code&gt;가 &lt;strong&gt;인터셉트할 주소를 설정&lt;/strong&gt;한다.&lt;/p&gt;

&lt;p&gt;Spring Security에서 인가코드 발급을 위해 사용되는 URI는 &lt;strong&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2AuthorizationRequestRedirectFilter&lt;/code&gt;의&lt;/strong&gt; &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DEFAULT_AUTHORIZATION_REQUEST_BASE_URI&lt;/code&gt; 이다. 해당  상수는 &lt;em&gt;/oauth2/authorization&lt;/em&gt;라는 값으로 설정된다.&lt;/p&gt;

&lt;p&gt;또한 인가코드 발급 후, 기본적으로 리다이렉션 되는 주소는 &lt;strong&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationFilter&lt;/code&gt;&lt;/strong&gt;의 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DEFAULT_FILTER_PROCESSES_URI&lt;/code&gt;이다. 해당 상수는 &lt;em&gt;/login/oauth2/code&lt;/em&gt;로 설정된다.&lt;/p&gt;

&lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Oauth2LoginConfigure&lt;/code&gt;는 configure&lpar;&rpar; 메서드를 통해 만일 사용자가 &lt;strong&gt;커스텀으로 작성한 인가코드 발급 URI과 Redirection URI가 존재한다면 해당 주소로 수정하고, 만일 존재하지 않는다면 기본주소를 사용하도록 설정한다&lt;/strong&gt;.&lt;/p&gt;

&lt;h1 id=&quot;spring-security-oauth2-인증-처리-흐름&quot;&gt;Spring Security OAuth2 인증 처리 흐름&lt;/h1&gt;

&lt;p&gt;Sequence 다이어그램의 형태를 흉내내어 정리하긴 했지만 가독성 문제로 일부 클래스들은 생략된 상태라는점 참고해주길 바란다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h2 id=&quot;인가코드-발급&quot;&gt;인가코드 발급&lt;/h2&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/313c33ea-f99b-4fd4-a0da-c067d4a90160&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;ol&gt;
  &lt;li&gt;로그인 버튼을 누르면 클라이언트는 &lt;em&gt;/oauth2/authorization&lt;/em&gt; 또는 커스텀된 인가코드 요청 uri로 요청을 보낸다.&lt;/li&gt;
  &lt;li&gt;&lt;em&gt;/oauth2/authorization&lt;/em&gt;로 오는 요청은 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2AuthorizationRequestRedirectFilter&lt;/code&gt;에 의해 인터셉트 된다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2AuthorizationRequestRedirectFilter&lt;/code&gt;은 리다이렉션 URI&lpar;&lt;em&gt;/login/oauth2/code&lt;/em&gt;&rpar;를 Query Parameter로 사용하여 Google에 인가 코드를 요청한다.&lt;/li&gt;
&lt;/ol&gt;

&lt;h2 id=&quot;토큰-발급&quot;&gt;토큰 발급&lt;/h2&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/4ef6889f-0b9e-4f6f-ab52-ca3c32126aeb&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;ol&gt;
  &lt;li&gt;Google은 &lt;strong&gt;인가코드&lt;/strong&gt;를 Query Parameter로 사용하여 리다이렉션 URI &lt;em&gt;/login/oauth2/code&lt;/em&gt;로 리다이렉션 한다.&lt;/li&gt;
  &lt;li&gt;&lt;em&gt;/login/oauth2/code&lt;/em&gt;로 리다이렉션된 요청은 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationFilter&lt;/code&gt;에 의해 인터셉트 된다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationProvider&lt;/code&gt;가 인가코드를 사용하여 엑세스 토큰을 요청하고, 엑세스 토큰을 사용하여 사용자 정보를 요청한다.&lt;/li&gt;
&lt;/ol&gt;

&lt;h2 id=&quot;사용자-정보-저장&quot;&gt;사용자 정보 저장&lt;/h2&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/19f7f0cf-3016-482b-9b4f-c27ebe0b78e1&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;ol&gt;
  &lt;li&gt;사용자 정보를 요청받은 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Oauth2UserService&lt;/code&gt;는 엑세스 토큰을 사용하여 Google에 사용자 정보를 요청한다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Oauth2UserService&lt;/code&gt;가 Google에서 반환받은 사용자 정보를 OAuth2User 형태로 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationProvider&lt;/code&gt;에 반환한다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationProvider&lt;/code&gt;가 사용자 정보를 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2LoginAuthenticationFilter&lt;/code&gt;에 반환한다. 이때 반환되는 OAuth2LoginAuthenticationToken은 &lt;strong&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Authentication&lt;/code&gt;&lt;/strong&gt;의 구현체이다.&lt;/li&gt;
  &lt;li&gt;&lt;strong&gt;SecurityContext 내에Authentication 객체가 저장된다.&lt;/strong&gt;&lt;/li&gt;
  &lt;li&gt;LoginSuccessHandler가 실행된다.&lt;/li&gt;
&lt;/ol&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h1 id=&quot;코드&quot;&gt;코드&lt;/h1&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h2 id=&quot;security-config&quot;&gt;Security Config&lt;/h2&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;nd&quot;&gt;@Configuration&lt;/span&gt;
&lt;span class=&quot;nd&quot;&gt;@EnableWebSecurity&lt;/span&gt;
&lt;span class=&quot;nd&quot;&gt;@RequiredArgsConstructor&lt;/span&gt;
&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Oauth2ClientConfig&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

    &lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;final&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2UserService&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2UserService&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;final&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;LoginSuccessHandler&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;loginSuccessHandler&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Bean&lt;/span&gt;
    &lt;span class=&quot;nc&quot;&gt;SecurityFilterChain&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;securityFilterChane&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;HttpSecurity&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;http&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;throws&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Exception&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;c1&quot;&gt;// 사용자가 특정 URL에 접근할 수 있는 권한 설정&lt;/span&gt;
        &lt;span class=&quot;n&quot;&gt;http&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;authorizeHttpRequests&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;requests&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;-&amp;gt;&lt;/span&gt;
                &lt;span class=&quot;n&quot;&gt;requests&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;requestMatchers&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;s&quot;&gt;&quot;/**&quot;&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;s&quot;&gt;&quot;/api-docs/**&quot;&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;s&quot;&gt;&quot;/swagger-ui/**&quot;&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;permitAll&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt;
        &lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;

        &lt;span class=&quot;n&quot;&gt;http&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;csrf&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nl&quot;&gt;AbstractHttpConfigurer:&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;:&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;disable&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;

        &lt;span class=&quot;n&quot;&gt;http&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;oauth2Login&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;oauth2&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;-&amp;gt;&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oauth2&lt;/span&gt;
                &lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;userInfoEndpoint&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;userInfoEndpointConfig&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;-&amp;gt;&lt;/span&gt;
                        &lt;span class=&quot;n&quot;&gt;userInfoEndpointConfig&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;userService&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;oAuth2UserService&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&rpar;&lt;/span&gt;
                &lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;successHandler&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;loginSuccessHandler&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt;
                &lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;failureUrl&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;s&quot;&gt;&quot;http://localhost:3000&quot;&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt;
        &lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;

        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;http&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;build&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;ul&gt;
  &lt;li&gt;&lt;strong&gt;http.authorizeHttpRequests&lt;/strong&gt;: 사용자가 특정 URL에 접근할 수 있는 권한을 설정한다.
    &lt;ul&gt;
      &lt;li&gt;로그인 없이도 조회가 가능한 사이트이기 때문에 모든 경로에 대한 접근을 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;permitAll&lpar;&rpar;&lt;/code&gt;로 설정했다.&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;&lt;strong&gt;http.csrf&lpar;&rpar;.disable&lpar;&rpar;&lt;/strong&gt;: CSRF 보호 설정을 disable한다.
    &lt;ul&gt;
      &lt;li&gt;RESTful API 에서는 따로 CSRF가 필요없다.&lt;/li&gt;
      &lt;li&gt;클라이언트 요청에 대해서는 따로 JWT를 사용하여 CSRF 토큰을 대체한다. &lpar;다른 포스팅에서 작성&rpar;&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;&lt;strong&gt;oauth2Login&lt;/strong&gt;: Spring Security에서 사용하는 인스턴스를 초기화 및 커스텀 URI를 설정한다.
    &lt;ul&gt;
      &lt;li&gt;사용자 정보 요청시 사용할 커스텀 클래스를 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;oAuth2UserService&lt;/code&gt;로 설정했다.&lt;/li&gt;
      &lt;li&gt;로그인 성공시 커스텀한 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;LoginSuccessHandler&lt;/code&gt;가 실행되도록 설정했다.&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt;

&lt;h2 id=&quot;oauth2userservice&quot;&gt;oAuth2UserService&lt;/h2&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/ea0f3b13-28a2-4126-9602-3edfc59bd06a&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;추후 다른 OAuth2 서비스가 추가되어도 코드 변경 없이 사용할 수 있도록 interface를 사용했다.&lt;/p&gt;

&lt;ul&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;ProviderUser&lt;/code&gt;: 애플리케이션에서 필요한 사용자 속성을 정의한다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2ProviderUser&lt;/code&gt;: 추상 클래스로, 모든 OAuth2 서비스에서 동일한 형태로 제공되는 속성을 받아오는 메서드를 구현한다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;GoogleUser&lt;/code&gt;: GoogleUser 객체를 저장하는 클래스로, OAuth2ProviderUser에서 구현되지 않은 메서드를 구현한다.&lt;/li&gt;
&lt;/ul&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;nd&quot;&gt;@Slf4j&lt;/span&gt;
&lt;span class=&quot;nd&quot;&gt;@Service&lt;/span&gt;
&lt;span class=&quot;nd&quot;&gt;@Transactional&lt;/span&gt;
&lt;span class=&quot;nd&quot;&gt;@RequiredArgsConstructor&lt;/span&gt;
&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2UserService&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;extends&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;DefaultOAuth2UserService&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

    &lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;final&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ArtistService&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;artistService&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;

    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2User&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;loadUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;OAuth2UserRequest&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;userRequest&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;throws&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2AuthenticationException&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;nc&quot;&gt;ClientRegistration&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;userRequest&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getClientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
        &lt;span class=&quot;nc&quot;&gt;OAuth2User&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;super&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;loadUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;userRequest&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//사용자 정보 반환&lt;/span&gt;
        &lt;span class=&quot;nc&quot;&gt;ProviderUser&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;providerUser&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;providerUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
        &lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;registrationId&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;userRequest&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getClientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getRegistrationId&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
        &lt;span class=&quot;n&quot;&gt;artistService&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;register&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;registrationId&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;providerUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
        &lt;span class=&quot;n&quot;&gt;log&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;info&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;s&quot;&gt;&quot;회원가입 = &quot;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;+&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;providerUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getName&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;;&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;providerUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ProviderUser&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;providerUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;ClientRegistration&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2User&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;registrationId&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getRegistrationId&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;registrationId&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;equals&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;s&quot;&gt;&quot;google&quot;&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
            &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;GoogleUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
        &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;kc&quot;&gt;null&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//todo: 예외 반환&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;프론트에서  &lt;em&gt;/oauth2/authorization&lt;/em&gt; 로 인가코드 요청을 보내면, 사용자 정보 반환을 위하여 커스텀된 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2UserService&lt;/code&gt;가 실행된다.&lt;/p&gt;

&lt;ul&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;super.loadUser&lt;/code&gt;: DefaultOAuth2UserService의 loadUser&lpar;&rpar;을 실행시킨다.
    &lt;ul&gt;
      &lt;li&gt;사용자 속성&lpar;attributes&rpar;과 사용자 권한&lpar;authorities&rpar;이 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OAuth2User&lt;/code&gt; 형태로 리턴된다.&lt;/li&gt;
      &lt;li&gt;
        &lt;p&gt;google에서 제공받는 attributes는 아래와 같다.&lt;/p&gt;

        &lt;blockquote&gt;
          &lt;p&gt;{sub= …, name=임연후, given_name=연후, family_name=임, picture=https://…, email=yeonnu82g@gmail.com, email_verified=true}&lt;/p&gt;

        &lt;/blockquote&gt;
      &lt;/li&gt;
    &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;providerUser&lpar;clientRegistration, oAuth2User&rpar;&lt;/code&gt;: 제공받은 사용자 정보를 각 서비스에 맞는 객체&lpar;GoogleUser, NaberUser….&rpar; 로 변환시킨다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;artistService.register&lt;/code&gt;: 제공받은 객체를 사용하여 실제 회원가입을 구현한다.&lt;/li&gt;
&lt;/ul&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;abstract&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2ProviderUser&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;implements&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ProviderUser&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

    &lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;final&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Map&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;lt;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Object&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;gt;&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;attributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;final&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2User&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;final&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ClientRegistration&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;

    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;OAuth2ProviderUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Map&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;lt;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Object&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;gt;&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;attributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2User&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt;
                              &lt;span class=&quot;nc&quot;&gt;ClientRegistration&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;attributes&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;attributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;oAuth2User&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;clientRegistration&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getPassword&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;no&quot;&gt;UUID&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;randomUUID&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;toString&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getEmail&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getAttributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;get&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;s&quot;&gt;&quot;email&quot;&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;toString&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getProvider&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getRegistrationId&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;List&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;lt;?&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;extends&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;GrantedAuthority&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;gt;&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getAuthorities&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getAuthorities&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;stream&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt;
                &lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;map&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;authority&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;-&amp;gt;&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;SimpleGrantedAuthority&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;authority&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getAuthority&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;&rpar;&lt;/span&gt;
                &lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;toList&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Map&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;lt;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Object&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;gt;&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getAttributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;attributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;GoogleUser&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;extends&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OAuth2ProviderUser&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;GoogleUser&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;OAuth2User&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ClientRegistration&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;kd&quot;&gt;super&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getAttributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;oAuth2User&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;clientRegistration&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getId&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getAttributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;get&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;s&quot;&gt;&quot;sub&quot;&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;toString&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getName&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getAttributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;get&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;s&quot;&gt;&quot;name&quot;&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;toString&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getPicture&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getAttributes&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;get&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;s&quot;&gt;&quot;picture&quot;&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;toString&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;이때 사용한 OAuth2ProviderUser와 GoogleUser는 위와 같다.&lt;/p&gt;

&lt;h1 id=&quot;결과&quot;&gt;결과&lt;/h1&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/a6263ba9-6d77-4ead-8eba-ac0142370922&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;Spring Security를 통해 정상적으로 사용자 정보를 제공받았다.&lt;/p&gt;

&lt;p&gt;다음에는 사용자의 uuid를 통해 JWT 토큰을 생성하고, JWT 토큰을 통해 사용자 요청을 검사하는 내용을 다뤄보겠다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;hr /&gt;

&lt;p&gt;공부를 하겠다고 Spring Security 인강을 꽤 비싼 돈 주고 사긴 했는데 그 분량이 만만찮아서 아직 일부밖에 듣지 못했다…
인강 설명을 참고하긴 했지만 직접 디버깅을 통해 공부한 내용이라 게시글에서 틀린 부분이 존재할 수 있다.
혹시 틀린 부분이 있다면 댓글로 알려주시면 감사하겠습니다.&lt;/p&gt;
 | 🗓️ 2024/10/12 <br>
 🍀 [디자인패턴&lpar;5&rpar;- DI&lpar;Dependency Injection&rpar;와 서비스 로케이터](https://lcqff.github.io/design-pattern-5/) | 👀 &lt;hr /&gt;

&lt;p&gt;이전 포스팅&lt;/p&gt;
&lt;ul&gt;
  &lt;li&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/08/19/design-pattern-1.html&quot;&gt;객체지향&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/09/24/design-pattern-2.html&quot;&gt;다형성과 추상 타입&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/09/30/design-pattern-3.html&quot;&gt;재사용: 상속보단 조립&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/10/01/design-pattern-4.html&quot;&gt;설계 원칙 SOLID&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;

&lt;hr /&gt;
&lt;h2 id=&quot;개요&quot;&gt;개요&lt;/h2&gt;

&lt;p&gt;소프트웨어는 두 개의 영역으로 구분할수 있다.&lt;/p&gt;

&lt;ul&gt;
  &lt;li&gt;&lt;strong&gt;어플리케이션 영역&lt;/strong&gt;: 고수준 정책 및 저수준 구현을 포함&lt;/li&gt;
  &lt;li&gt;&lt;strong&gt;메인 영역&lt;/strong&gt;: 어플리케이션이 동작하도록 각 객체들을 연결해주는 영역&lt;/li&gt;
&lt;/ul&gt;

&lt;p&gt;이때 DI&lpar;dependency injection: 의존성 주읩&rpar;은 메인영역에서 객체를 연결하기 위해 사용된다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;이번 포스팅에서는…&lt;/p&gt;

&lt;blockquote&gt;
  &lt;p&gt;어플리케이션 영역과 메인 영역의 차이를 학습한다.&lt;/p&gt;

  &lt;p&gt;객체 연결 방법인 서비스 로케이터와 의존성 주입&lpar;DI&rpar;에 대해 학습한다.&lt;/p&gt;

  &lt;p&gt;서비스 로케이터의 단점에 대해 학습한다.&lt;/p&gt;

  &lt;p&gt;의존성 주입 방법에 대해 학습한다.&lt;/p&gt;
&lt;/blockquote&gt;

&lt;h2 id=&quot;어플리케이션-영역과-메인-영역&quot;&gt;어플리케이션 영역과 메인 영역&lt;/h2&gt;

&lt;p&gt;이번 포스팅에선 학습을 위해 간단한 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;비디오 포맷 변환기&lt;/code&gt;예시코드를 작성한다. 
요구사항은 아래와 같다.&lt;/p&gt;

&lt;ul class=&quot;box-note&quot;&gt;
  &lt;li&gt;변환 작업을 요청하면 순차적으로 변환을 처리한다.
    &lt;ul&gt;
      &lt;li&gt;변환 요청 정보는 &lt;strong&gt;파일&lt;/strong&gt; 또는 &lt;strong&gt;DB&lt;/strong&gt;를 이용하여 보관할 수 있다.&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;비디오의 변환 처리는 오픈 소스인 &lt;strong&gt;ffmpeg&lt;/strong&gt;를 사용하거나 구매 예정인 &lt;strong&gt;변환 솔루션&lt;/strong&gt;을 사용할 수 있다.&lt;/li&gt;
  &lt;li&gt;명령행에서 변환할 source 파일과 변환 결과인 targer 파일을 입력한다.&lt;/li&gt;
&lt;/ul&gt;

&lt;h3 id=&quot;어플리케이션-영역&quot;&gt;어플리케이션 영역&lt;/h3&gt;

&lt;p&gt;위 요구사항을 설계로 옮기면 아래 이미지와 같다.&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/2f600066-2924-4656-902a-e48bef8231f3&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/10/01/design-pattern-4.html&quot;&gt;개방 폐쇄 원칙&lt;/a&gt;을 지키기 위하여 작업을 처리하는 기능과 비디오 변환 기능을 Interface로 구현하였다. 
이로써 작업 처리 방식과 비디오 변환 방식이 추가되어도 transcoder 패키지의 변경은 발생하지 않을 것이다.&lt;/p&gt;

&lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;JobQueue&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Transcoder&lt;/code&gt;을 사용하여 실제 기능을 구현한 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Worker&lt;/code&gt; 클래스는 아래와 같다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;...&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//JobQueue을 구현한 콘크리트 객체를 구한다.&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;...&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;// Transcoder을 구현한 콘크리트 객체를 구한다.&lt;/span&gt;
		
		&lt;span class=&quot;k&quot;&gt;while&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;...&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;nc&quot;&gt;JobData&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobdata&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getJob&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;transcode&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;jobData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getSource&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getTarget&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;이때 worker가 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;FileJobQueue&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DBJobQueue&lt;/code&gt;와 같은 콘크리트 객체를 의존하는 경우, &lt;red&gt;순환의존의 문제&lt;/red&gt;가 발생한다.&lt;/p&gt;

&lt;p&gt;transcoder 패키지를 의존하고 있는 다른 패키지를 의존하게 되기 때문이다.&lt;/p&gt;

&lt;p&gt;또한 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;FileJobQueue&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DbJobQueue&lt;/code&gt;는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;JobQueue&lt;/code&gt;를 구현한 &lt;strong&gt;하위 모듈&lt;/strong&gt;이기에, 상위 모듈 Worker가 하위모듈을 의존하게 되어 &lt;red&gt;의존 역전 법칙을 위반&lt;/red&gt;하게 된다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/bdecdeec-5dce-418d-be7e-6b229bc469b3&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;이러한 두 문제는 &lt;strong&gt;JobQueue구현체를 제공하는 클래스를 transcoder 패키지 안에 포함시키는 방법&lt;/strong&gt;으로 해결할 수 있다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/95030aa2-c945-4d72-8784-995e8067a0a3&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Locator&lt;/code&gt;는 Worker에 필요한 &lt;strong&gt;JobQueue와 Transcoder의 구현체를 반환하는 역할&lt;/strong&gt;을 한다. 이로써 순환의존 문제와 의존 역전 법칙 위반 문제를 해결할 수 있었다.&lt;/p&gt;

&lt;p&gt;실제 구현 코드는 아래와 같다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getInstance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getInstance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getTanscoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		
		&lt;span class=&quot;k&quot;&gt;while&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;...&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;nc&quot;&gt;JobData&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobdata&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getJob&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;transcode&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;jobData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getSource&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getTarget&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;instance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getInstance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;instance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;init&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;instance&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;locator&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobqueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobqueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;transcodeer&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
		
	&lt;span class=&quot;c1&quot;&gt;// ... getter&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;이렇게 &lt;strong&gt;사용할 객체를 제공하는 책임을 갖는 객체&lt;/strong&gt;를 &lt;blue&gt;서비스 로케이터&lpar;Service Locator&rpar;&lt;/blue&gt;라 한다.&lt;/p&gt;

&lt;div class=&quot;callout&quot;&gt;
  &lt;div&gt;💡&lt;/div&gt;
  &lt;div&gt;
	&lt;strong&gt;서비스 로케이터&lpar;Service Locator&rpar;&lt;/strong&gt;&lt;br /&gt;
    사용할 객체를 제공하는 책임을 가지는 객체
  &lt;/div&gt;
&lt;/div&gt;

&lt;h3 id=&quot;메인영역&quot;&gt;메인영역&lt;/h3&gt;

&lt;p&gt;어플리케이션 영역에서 우리는 Locator을 사용하여 Worker에 콘크리트 객체를 할당해주었다.&lt;/p&gt;

&lt;p&gt;그렇다면 Locator는 언제 초기화되는가? 
즉, &lt;strong&gt;어플리케이션 영역에서 사용되는 객체의 생성&lt;/strong&gt;은 누가 담당하는가? 바로 메인 영역이다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;메인 영역의 책임은 아래와 같다.&lt;/p&gt;

&lt;ul&gt;
  &lt;li&gt;어플리케이션 영역에서 사용될 객체를 생성한다.&lt;/li&gt;
  &lt;li&gt;각 객체간의 의존 관계를 설정한다.&lt;/li&gt;
  &lt;li&gt;어플리케이션을 실행한다.&lt;/li&gt;
&lt;/ul&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;args&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;//상위 수준 모듈 transcoder 패키지에서 사용할 하위 모듈 생성	&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;FileJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	
		&lt;span class=&quot;c1&quot;&gt;//Locator 초기화&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;locator&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;init&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		
		&lt;span class=&quot;c1&quot;&gt;//상위 수준 모듈 생성 및 실행&lt;/span&gt;
		&lt;span class=&quot;kd&quot;&gt;final&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Thread&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;t&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Thread&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Runnable&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
				&lt;span class=&quot;n&quot;&gt;workder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
			&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;위는 메인 영역에서 사용되는 Main 클래스 코드이다.&lt;/p&gt;

&lt;p&gt;transcoder 패키지에서 필요로 하는 &lt;strong&gt;하위 모듈을 생성&lt;/strong&gt;하고 &lt;strong&gt;Locator에 이를 할당&lt;/strong&gt;해주는 것으로 어플리케이션 영역에서 사용되는 객체의 &lt;strong&gt;의존관계를 설정&lt;/strong&gt;해주었다.&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/ecea04e0-44fb-45c0-b9cf-7a6902186aa3&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;이러한 설계를 통해 만일 어플리케이션 영역에서 사용하는 하위 수준의 모듈의 변경은 메인 영역을 수정하는 것으로 해결할 수 있다.&lt;/p&gt;

&lt;p&gt;&lt;strong&gt;모든 의존은 메인 영역에서 어플리케이션 영역으로 향한다&lt;/strong&gt;. 역방향의 의존은 발생하지 않는다.&lt;/p&gt;

&lt;p&gt;즉, 메인 영역의 코드를 변경이 어플리케이션 영역의 코드 변경을 야기하지 않는다.&lt;/p&gt;

&lt;h3 id=&quot;서비스-로케이터의-단점&quot;&gt;서비스 로케이터의 단점&lt;/h3&gt;

&lt;p&gt;위 예시에서는 &lt;strong&gt;서비스 로케이터&lt;/strong&gt;를 이용하여 각 객체간 의존관계를 설정했다.&lt;/p&gt;

&lt;p&gt;그러나 서비스 로케이터를 사용하는 방식은 방식은 몇가지 단점이 존재한다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;ul&gt;
  &lt;li&gt;&lt;strong&gt;서비스 로케이터는 동일 타입의 객체가 다수 필요한 경우 각 객체별로 제공 메서드를 만들어주어야 한다.&lt;/strong&gt;&lt;/li&gt;
&lt;/ul&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;fileJobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getJobQueue1&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;dbJobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getJobQueue2&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// ...	&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue1&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue2&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue1&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue2&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;jobQueue1&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue1&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;jobQueue2&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue2&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
		
	&lt;span class=&quot;c1&quot;&gt;// ... getter&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;그렇다면 getJobQueue1, getJobQueue2라는 이름 대신에 getFileJobQueue, getDbJobQueue라는 이름을 쓸 순 없는걸까?&lt;/p&gt;

&lt;p&gt;이를태면 아래와 같이 특정 조건에 따라 fileJobQueue를 사용할수도, dbJobQueue을 사용할수도 있는 Worker 클래스가 있다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
		
		
		&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;someCondition&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;?&lt;/span&gt; 
			&lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getFileJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;:&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getDbJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		
		&lt;span class=&quot;c1&quot;&gt;// ...	&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;그러나 이러한 사용은 결국 Worker 클래스가 JobQueue 구현 객체에 의존하도록 만든다. 
만일 File이나 DB가 아닌 새로운 기능이 추가되는 경우, Worker 클래스의 변경이 발생하게 된다는 것이다. 
즉 개방 폐쇄 원칙을 위반한다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;ul&gt;
  &lt;li&gt;&lt;strong&gt;인터페이스 분리 원칙을 위반한다.&lt;/strong&gt;&lt;/li&gt;
&lt;/ul&gt;

&lt;div class=&quot;callout&quot;&gt;
  &lt;div&gt;💡&lt;/div&gt;
  &lt;div&gt;
	&lt;strong&gt;인터페이스 분리 원칙 &lpar;ISP&rpar;&lt;/strong&gt;&lt;br /&gt;
    클라이언트는 자신이 사용하지 않는 인터페이스에 의존하지 않는다.
  &lt;/div&gt;
&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;instance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getInstance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;instance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;c1&quot;&gt;// ....&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getInstance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Locator&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getInstance&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getTanscoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// Worker는 Locator에서ㅓ 제공하는 모든 타입에 접근할수 있게 된다. &lt;/span&gt;
	
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;서비스 로케이터를 사용하는 객체는 자신이 필요한 타입 뿐만 아니라 서비스 로케이터가 제공하는 모든 타입을 사용할수 있다. 
이렇게 발생하는 &lt;strong&gt;불필요한 의존&lt;/strong&gt;으로 인해 다른 의존 객체에 의해 발생하는 변경에 영향을 받을 수 있다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;이러한 단점들 때문에 일반적으로는 서비스 로케이터 대신, 외부에서 객체를 주입해주는 &lt;strong&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DI&lpar;Dependency Injection&rpar;&lt;/code&gt;&lt;/strong&gt;이 사용된다.&lt;/p&gt;

&lt;h2 id=&quot;의존성-주입을-사용한-의존-객체-사용&quot;&gt;의존성 주입을 사용한 의존 객체 사용&lt;/h2&gt;

&lt;div class=&quot;callout&quot;&gt;
  &lt;div&gt;💡&lt;/div&gt;
  &lt;div&gt;
	&lt;strong&gt;의존성 주입&lpar;DI; Dependency Injection&rpar;&lt;/strong&gt;&lt;br /&gt;
    필요한 객체를 직접 생성하거나 찾지 않고 외부에서 넣어주는 방식
  &lt;/div&gt;
&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;DI는 서비스 로케이터의 단점을 보완하기 위한 방법으로 그 구현 자체는 단순하다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;Worker&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcodeer&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;transcoder&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=.&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;args&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;//상위 수준 모듈 transcoder 패키지에서 사용할 하위 모듈 생성	&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;FileJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		
		&lt;span class=&quot;c1&quot;&gt;//상위 수준 모듈 생성 및 실행&lt;/span&gt;
		&lt;span class=&quot;kd&quot;&gt;final&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		
		&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;worker 객체는 스스로 의존하는 객체를 찾거나 생성하는 과정 없이 &lt;strong&gt;외부의 main 메서드에서 생성자를 통해 사용할 객체를 주입&lt;/strong&gt;받는다.&lt;/p&gt;

&lt;p&gt;이렇게 외부의 누군가에게 의존할 객체를 주입받는 것을 &lt;strong&gt;의존성 주입&lt;/strong&gt;이라 한다.&lt;/p&gt;

&lt;h3 id=&quot;조립기&quot;&gt;조립기&lt;/h3&gt;

&lt;p&gt;DI를 사용할시 각 객체들을 생성하고, 의존 관계에 따라 연결해주는 &lt;strong&gt;조립기&lt;/strong&gt;가 필요하다.&lt;/p&gt;

&lt;p&gt;위 예제에서는 Main이 객체의 실행과 더불어 조립기의 역할을 하고 있지만 조립기를 별도로 분리하면 조립기 구현 변경의 유연성을 얻을 수 있다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Assembler&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;createAndWrite&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQeue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;FileJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;FfmpegTranscoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;jobQeue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;c1&quot;&gt;// ...getter&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;args&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Assember&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;assembler&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Assembler&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;assembler&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;createAndWire&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		
		&lt;span class=&quot;kd&quot;&gt;final&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;assembler&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getWorker&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		
		&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;h2 id=&quot;의존성-주입-방식&quot;&gt;의존성 주입 방식&lt;/h2&gt;

&lt;h3 id=&quot;생성자-주입constructor-injection&quot;&gt;생성자 주입&lpar;Constructor Injection&rpar;&lt;/h3&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;Worker&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcodeer&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;transcoder&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=.&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;ul&gt;
  &lt;li&gt;생성자를 통해 의존 객체를 전달받는다.&lt;/li&gt;
  &lt;li&gt;객체 생성 시점에서 의존 객체의 오류를 검증할 수 있다.&lt;/li&gt;
  &lt;li&gt;의존 객체가 먼저 생성되어야만 사용할 수있다.
    &lt;ul&gt;
      &lt;li&gt;객체의 생성이 객체의 정상 동작을 보장한다.&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt;

&lt;h3 id=&quot;세터-주입setter-injection&quot;&gt;세터 주입&lpar;Setter Injection&rpar;&lt;/h3&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;setJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;jobQueue&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;ul&gt;
  &lt;li&gt;객체가 완전히 초기화되지 않은 상태로 사용될 수 있다.
    &lt;ul&gt;
      &lt;li&gt;객체의 생성이 객체의 정상 동작을 보장할 수 없다.&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt;

&lt;h3 id=&quot;필드-주입field-injection&quot;&gt;필드 주입&lpar;Field Injection&rpar;&lt;/h3&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;nd&quot;&gt;@Autowired&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;jobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;nd&quot;&gt;@Autowired&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;transcoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;ul&gt;
  &lt;li&gt;프레임워크에서 주로 사용된다.&lt;/li&gt;
  &lt;li&gt;코드가 간결해지나 의존성 주입이 명확하게 드러나지 않는다&lt;/li&gt;
  &lt;li&gt;테스트 시 의존성을 설정하기가 어렵다.&lt;/li&gt;
&lt;/ul&gt;

&lt;h2 id=&quot;di와-테스트&quot;&gt;DI와 테스트&lt;/h2&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/55225b75-9aa5-4059-8bfb-a2bb1c45a471&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;위와 같은 구조에서, &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Worker&lt;/code&gt;를 테스트하기 위해서는 JobQueue의 구현체와 Transcoder의 구현체가 필요하다.&lt;/p&gt;

&lt;p&gt;JobQueue와 Transcoder의 구현체가 완성돼있지 않은 상태에서, &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Worker&lt;/code&gt;가 &lt;strong&gt;의존성 주입&lt;/strong&gt;을 사용하고 있다면 단순히 Workder에 JobQueue 구현체의 Mock 객체와 Transcoder의 &lt;strong&gt;Mock 객체&lt;/strong&gt;를 전달하는 것으로 해결할 수 있다.&lt;/p&gt;

&lt;p&gt;이렇게 의존성 주입은 테스트의 편의성을 제공하기도 한다.&lt;/p&gt;

&lt;h2 id=&quot;스프링에서의-의존성-주입&quot;&gt;스프링에서의 의존성 주입&lt;/h2&gt;

&lt;p&gt;의존성 주입&lpar;DI&rpar;은 스프링이 제공하는 핵심 기능 중 하나이다.&lt;/p&gt;

&lt;p&gt;&lt;strong&gt;스프링 프레임워크&lt;/strong&gt;와 &lt;strong&gt;스프링 부트&lt;/strong&gt;는 모두 DI를 지원하며, 스프링의 핵심 컨테이너인 &lt;strong&gt;IoC&lpar;Inversion of Control&rpar;&lt;/strong&gt; 컨테이너를 통해 DI를 구현한다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;nd&quot;&gt;@Configuration&lt;/span&gt;
&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;TranscoderConfig&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;

	&lt;span class=&quot;nd&quot;&gt;@Bean&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;JobQueue&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;fileJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;FileJobQueue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;nd&quot;&gt;@Bean&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Transcoder&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;ffmpegTranscoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;FfmpegTranscoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;nd&quot;&gt;@Bean&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Workder&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;worker&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;Worker&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;fileJobQUeue&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;,&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;ffmpegTranscoder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;위는 스프링 프레임워크를 사용한 의존성 주입의 예시이다.&lt;/p&gt;

&lt;ul&gt;
  &lt;li&gt;개발자가 모든 Bean과 그 관계를 직접 정의한다.&lt;/li&gt;
  &lt;li&gt;외부 종속성의 경우 DI 설정파일에서 의존성을 주입해야한다.&lt;/li&gt;
&lt;/ul&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;nd&quot;&gt;@SpringBootApplication&lt;/span&gt;
&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;MyApplication&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;args&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;nc&quot;&gt;SpringApplication&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;run&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;MyApplication&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;class&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;args&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;&lt;strong&gt;스프링 부트&lt;/strong&gt;는 스프링 프레임워크의 설정을 간소화하고, 빠르게 애플리케이션을 구축할 수 있도록 돕는 도구로, 의존성 설정 또한 &lt;strong&gt;자동으로 설정 및 관리&lt;/strong&gt;된다.&lt;/p&gt;

&lt;p&gt;위 코드는 스프링 부트를 사용한 의존성 주입의 예시이다.&lt;/p&gt;

&lt;ul&gt;
  &lt;li&gt;별도의 Bean 설정이 필요하지 않는다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;@SpringBootApplication&lt;/code&gt; 어노테이션을 사용하여 프로젝트 내의 모든 빈과 외부 종속성을 자동으로 탐색 및 등록한다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;spring-boot-starter-web&lt;/code&gt;과 같은 스타터 패키지를 제공하여 해당 패키지 사용시 자동으로 MVC 관련 빈들이 등록된다.&lt;/li&gt;
  &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;@SpringBootTest&lt;/code&gt; 어노테이션을 사용하면 테스트시에도 자동으로 DI를 처리해준다.&lt;/li&gt;
&lt;/ul&gt;
 | 🗓️ 2024/10/08 <br>
 🔥 [디자인패턴&lpar;4&rpar;- 설계 원칙: SOLID](https://lcqff.github.io/design-pattern-4/) | 👀 &lt;hr /&gt;

&lt;p&gt;이전 포스팅&lt;/p&gt;
&lt;ul&gt;
  &lt;li&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/08/19/design-pattern-1.html&quot;&gt;객체지향&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/09/24/design-pattern-2.html&quot;&gt;다형성과 추상 타입&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/09/30/design-pattern-3.html&quot;&gt;재사용: 상속보단 조립&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;

&lt;hr /&gt;
&lt;h2 id=&quot;개요&quot;&gt;개요&lt;/h2&gt;

&lt;p&gt;앞서 객체지향의 기본이 되는 책임 할당, 캡슐화, 다형성과 추상화, 조립을 통한 재사용에 대해 알아봤듯이 객체지향 설계는 소프트웨어의 변경을 유연하도록 돕는다.&lt;/p&gt;

&lt;p&gt;&lt;strong&gt;SOLID&lt;/strong&gt;는 이러한 객체 지향적인 설계를 돕는 설계 원칙이다.&lt;/p&gt;

&lt;p&gt;SOLID는 앞서 살펴본 책임 할당, 캡슐화, 다형성과 추상화, 조립을 통한 재사용과 같은 내용들을 체계적으로 정리한 것이다.&lt;/p&gt;

&lt;ul class=&quot;box-yello&quot;&gt;
  &lt;li&gt;단일 책임 원칙 &lpar;Single responseibility principle: SRP&rpar;&lt;/li&gt;
  &lt;li&gt;개방-폐쇄 원칙 &lpar;Open-closed principle: OCP&rpar;&lt;/li&gt;
  &lt;li&gt;리스코프 치환 원칙 &lpar;Liskov subsitution principle: LSP&rpar;&lt;/li&gt;
  &lt;li&gt;인터페이스 분리 원칙 &lpar;Interface segregation principle: ISP&rpar;&lt;/li&gt;
  &lt;li&gt;의존 역전 원칙 &lpar;Depencency inversion principle: DIP&rpar;&lt;/li&gt;
&lt;/ul&gt;

&lt;h2 id=&quot;단일-책임-원칙&quot;&gt;단일 책임 원칙&lt;/h2&gt;

&lt;blockquote&gt;
  &lt;p&gt;클래스는 단 한 개의 책임을 가져야 한다.&lt;/p&gt;

  &lt;p&gt;즉, 클래스를 변경하는 이유는 단 한개여야 한다.&lt;/p&gt;
&lt;/blockquote&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;DataViewer&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;display&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;loadHtml&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;updateGui&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;loadHtml&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//HTTP 응답을 반환한다.&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;HttpClient&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;client&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;HttpClient&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;client&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;connect&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;url&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;client&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getResponse&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;updateGui&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;// HTML 문자열을 GUI형태로 보여준다. &lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;GuiData&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;guiModel&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;parseDataToGuiData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;tableUI&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;changeData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;guiModel&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
		
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;GuiData&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;parseDataToGuiData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;
&lt;cap&gt;HTTP 프로토콜을 사용하여 데이터를 읽어와 화면에 보여주는 클래스&lt;/cap&gt;
&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;DataViewer클래스는 HTTP 응답을 받을 뿐만 아니라, 이를 화면에 보여주는 두 가지 책임을 지니고 있다.&lt;/p&gt;

&lt;p&gt;그렇다면 만일 서버에서 제공하는 데이터가 HTTP가 아닌 다른 형태로 바뀐다면 어떻게 될까?&lt;/p&gt;

&lt;h3 id=&quot;코드-수정의-어려움&quot;&gt;코드 수정의 어려움&lt;/h3&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;DataViewer&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;display&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;kt&quot;&gt;byte&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;load&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;updateGui&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;byte&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;loadHtml&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;// 로직 변경&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;SocketClient&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;client&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;SocketClient&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;client&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;connect&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;server&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;port&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;client&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;read&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;updateGui&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;kt&quot;&gt;byte&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;// 변경 발생&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;GuiData&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;guiModel&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;parseDataToGuiData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;tableUI&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;changeData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;guiModel&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;GuiData&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;parseDataToGuiData&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;kt&quot;&gt;byte&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//변경 발생&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;
&lt;cap&gt;HTTP → Socket으로 응답 데이터가 수정되었다.&lt;/cap&gt;
&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;HttpClient를 SocketClient로 교체한 것만으로도 해당 데이터를 사용하는 모든 메서드에 변경이 발생되었다.&lt;/p&gt;

&lt;p&gt;이러한 문제는 하나의 클래스가 데이터를 읽는 책임과 화면에 보여주는 책임, &lt;strong&gt;두가지의 책임을 지니고 있기 때문&lt;/strong&gt;이다.&lt;/p&gt;

&lt;p&gt;한 클래스가 지니는 책임의 개수가 많아질수록 한 책임의 기능 변화가 다른 책임에 주는 영향은 비례해서 증가한다. 즉, 코드를 절차지향적으로 만든다.&lt;/p&gt;

&lt;h3 id=&quot;재사용의-어려움&quot;&gt;재사용의 어려움&lt;/h3&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/4a472055-186b-41d1-932b-6390ddcc76e1&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DataViewer&lt;/code&gt;가 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;HttpClient&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;GuiComp&lt;/code&gt;라는 두 패키지를 사용한다고 하자. 또한 데이터를 읽어오는 기능이 필요한 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DataRequireClient&lt;/code&gt;가 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DataViewer&lt;/code&gt;을 사용하고 있다.&lt;/p&gt;

&lt;p&gt;이때 DataRequireClient가 필요한 것은 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DataViewer&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;HttpClient Jar 파일&lt;/code&gt;이나, DataViewer는 GuiComp를 사용하고 있으므로 실제로는 &lt;strong&gt;DataViewer와 HttpClient Jar 파일 뿐만 아니라 GuiComp의 Jar 파일까지 필요하게 된다.&lt;/strong&gt;&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/de076c98-e8c7-42d2-872f-e541b234dd1b&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;만일 단일 책임 원칙을 적용시켜 책임을 분리한다면 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DataRequireClient&lt;/code&gt;는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DataLoader&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;HttpClient 패키지&lt;/code&gt;만을 사용할 수 있게 된다.&lt;/p&gt;

&lt;h3 id=&quot;책임이란&quot;&gt;책임이란&lt;/h3&gt;

&lt;p&gt;객체의 존재 이유란, 책임을 할당하기 위함이다. ‘단일 책임 원칙’에서 우리는 한 객체는 하나의 책임만을 지녀야 한다는 개념을 배웠다.&lt;/p&gt;

&lt;p&gt;그러나 책임이란 것은 어떻게 구분하면 좋단 말인가?&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/2d4987a9-469a-49a4-9bc0-0ccb6cad6e14&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;위 이미지에서 GUIApplication은 DataViewer의 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;display&lpar;&rpar;&lt;/code&gt; 메서드를 사용하고 DataProcessor는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;loadData&lpar;&rpar;&lt;/code&gt;를 사용한다.&lt;/p&gt;

&lt;p&gt;만일 &lt;blue&gt;GUIApplication에서 요구되는 변경사항이 발생할 경우 DataViewer의 display&lpar;&rpar;가 변경될 확률이 높다.&lt;/blue&gt;&lt;/p&gt;

&lt;p&gt;또한 &lt;blue&gt;DataProcess에서 요구되는 변경사항이 발생할 경우 DataViewer의 loadData&lpar;&rpar;가 변경될 확률이 높아진다.&lt;/blue&gt;&lt;/p&gt;

&lt;p&gt;이렇게 &lt;strong&gt;서로 다른 클래스가 서로 다른 메서드를 사용하는 경우&lt;/strong&gt;, 이 메서드들은 각기 다른 책임을 지니고 있을 확률이 높다.&lt;/p&gt;

&lt;h2 id=&quot;개방-폐쇄-원칙&quot;&gt;개방 폐쇄 원칙&lt;/h2&gt;

&lt;blockquote&gt;
  &lt;p&gt;확장에는 열려 있어야하고, 변경에는 닫혀 있어야 한다.&lt;/p&gt;

  &lt;p&gt;즉, 기능을 변경하거나 확장할 수 있으면서 그 기능을 사용하는 코드는 수정하지 않는다.&lt;/p&gt;
&lt;/blockquote&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;기능을 변경하면서도 코드를 수정하지 않는다는 말이 생소하게 들릴 수 있으나, 이전에 한번 알아보았던 내용이다.&lt;/p&gt;

&lt;p&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/09/24/design-pattern-2.html&quot;&gt;다형성과 추상 타입&lt;/a&gt;에서 우리는 여러 종류의 Reservation을 DashboardHelper을 사용하여 출력하는 법에 대해 알아보았다.&lt;/p&gt;

&lt;h3 id=&quot;인터페이스를-통한-개방-폐쇄-원칙&quot;&gt;인터페이스를 통한 개방 폐쇄 원칙&lt;/h3&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/558e21f1-581e-4c52-a65e-24f25d699e89&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;위와 같은 구조의 코드에서 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DashboardHelper&lt;/code&gt;에 다른 Reservation을 추가해야하는 경우가 생기더라도, 우리는 코드의 수정 없이 &lt;red&gt;ReservationOrder를 상속받는 Reservation 클래스를 새로 만드는 것으로 기능 추가&lt;/red&gt; 를 할 수 있었다.&lt;/p&gt;

&lt;p&gt;즉, &lt;strong&gt;기능을 확장하면서도 기존의 코드에 대한 변경은 발생하지 않는다&lt;/strong&gt;.&lt;/p&gt;

&lt;p&gt;이러한 개방 폐쇄 원칙을 구현할 수 있는 이유는 &lt;strong&gt;변화되는 부분&lpar;위 그림에서는 Reservation을 읽어오는 부분&rpar;을 추상화&lt;/strong&gt; 했기 때문이다.&lt;/p&gt;

&lt;h3 id=&quot;상속을-통한-개방-폐쇄-원칙&quot;&gt;상속을 통한 개방 폐쇄 원칙&lt;/h3&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ResponseSender&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Data&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;ResponseSender&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Data&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;data&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;send&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;sendHeader&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;sendBody&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;	
	
	&lt;span class=&quot;kd&quot;&gt;protected&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;sendHeader&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// 헤더 데이터 전송&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;	
	
	&lt;span class=&quot;kd&quot;&gt;protected&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;sendBody&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// 바디 데이터 전송&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;위 예시는 HTTP 응답 데이터를 전송하는 클래스인 ResponseSender이다.&lt;/p&gt;

&lt;p&gt;눈여겨봐야 할 점은  &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;sendHeader&lpar;&rpar;&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;sendBody&lpar;&rpar;&lt;/code&gt;가 &lt;strong&gt;protected로 선언&lt;/strong&gt;되어있다는 점이다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ZippedResponseSender&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;extends&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ResponseSender&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;ZippedResponseSender&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Data&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;kd&quot;&gt;super&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;nd&quot;&gt;@Overried&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;protected&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;sendBody&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;//데이터 압축 처리&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;HTTP 응답 데이터를 전송할 뿐만 아니라, &lt;strong&gt;응답 데이터를 압축해서 전송할 수 있도록 기능을 확장&lt;/strong&gt;하려 한다.&lt;/p&gt;

&lt;p&gt;이를 위해서 ResponseSender의 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;sendBody&lpar;&rpar;&lt;/code&gt;를 오버라이드하여 압축 로직을 추가한 ZippedResponseSender클래스를 생성했다.&lt;/p&gt;

&lt;p&gt;이를 통해 기존 코드에 변경을 일으키지 않은 채, 압축 기능을 추가할 수 있다.&lt;/p&gt;

&lt;h3 id=&quot;개방-폐쇄-원칙의-위반&quot;&gt;개방 폐쇄 원칙의 위반&lt;/h3&gt;

&lt;p&gt;개방 폐쇄 원칙을 지키지 못한 코드에서는 여러가지 특징을 확인할 수 있다. 예시를 통해 이러한 특징을을 알아가보자.&lt;/p&gt;

&lt;h4 id=&quot;다운-캐스팅을-한다-instanceof을-사용한다&quot;&gt;다운 캐스팅을 한다, instanceof을 사용한다.&lt;/h4&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/29ae8803-4ce9-4214-a178-da9dbe959448&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;위와 같은 상속관계를 지니는 슈팅게임을 개발하려 한다. 이때, 화면에 캐릭터를 표시하는 코드가 아래와 같이 구현되었다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;drawCharacter&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Character&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;character&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;character&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;instanceof&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Missile&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;Missile&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;missile&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Missile&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;character&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//다운캐스팅&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;missile&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;drawSpecific&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;else&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;character&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;draw&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;
&lt;cap&gt;화면에 캐릭터를 표시하는 코드&lt;/cap&gt;
&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;만일 Character 타입이 Missile인 경우, 별도로 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;drawSpecific&lpar;&rpar;&lt;/code&gt; 메서드를 호출하도록 처리하고 있다.&lt;/p&gt;

&lt;p&gt;이러한 구현은 Character 클래스가 확장될 때 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;drawCharacter&lpar;&rpar;&lt;/code&gt; 메서드가 함께 수정될 가능성을 증가시킨다.&lt;/p&gt;

&lt;p&gt;즉 변경에 닫혀있지 않다.&lt;/p&gt;

&lt;h4 id=&quot;비슷한-if-else-블록이-존재한다&quot;&gt;비슷한 if-else 블록이 존재한다.&lt;/h4&gt;

&lt;p&gt;위의 예시에서, Enemy 캐릭터의 움직이는 경로를 패턴화하는 코드를 작성하려 한다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Enemy&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;extends&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Character&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;Enemy&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;pathPattern&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;draw&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;==&lt;/span&gt; &lt;span class=&quot;mi&quot;&gt;1&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;x&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;+=&lt;/span&gt; &lt;span class=&quot;mi&quot;&gt;4&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;else&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;==&lt;/span&gt; &lt;span class=&quot;mi&quot;&gt;2&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;y&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;+=&lt;/span&gt;&lt;span class=&quot;mi&quot;&gt;10&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;else&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;==&lt;/span&gt; &lt;span class=&quot;mi&quot;&gt;4&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;x&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;+=&lt;/span&gt; &lt;span class=&quot;mi&quot;&gt;4&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;y&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;+=&lt;/span&gt;&lt;span class=&quot;mi&quot;&gt;10&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;
&lt;cap&gt;Enemy 캐릭터의 움직이는 경로를 패턴화하는 코드&lt;/cap&gt;
&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;만일 Enemy 캐릭터에 새로운 경로 패턴을 추가하고 싶다면,  우리는 매번 새로운 if 블록을 추가하는 식으로 draw&lpar;&rpar; 메서드를 수정해야 한다. 즉, Enemy 클래스는 닫혀있지 않다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/48f0e1a8-4ad7-4923-a97d-97e311ea53ab&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Enemy&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;extends&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Character&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;PathPattern&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;Enemy&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;PathPattern&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;pathPattern&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;draw&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;x&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;nextX&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;y&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;pathPattern&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;nextY&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;위와 같이 PathPattern을 추상화 하는 것으로, 우리는 Enemy클래스의 변경 없이 새로운 경로 패턴을 추가할 수 있다.&lt;/p&gt;

&lt;h2 id=&quot;리스코프-치환-원칙&quot;&gt;리스코프 치환 원칙&lt;/h2&gt;

&lt;blockquote&gt;
  &lt;p&gt;상위 타입의 객체를 하위 타입의 객체로 치환해도 상위 타입을 사용하는 프로그램은 정상적으로 동작해야 한다.&lt;/p&gt;
&lt;/blockquote&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;리스코프 치환 원칙은 &lt;strong&gt;개방 폐쇄 원칙을 받쳐주는 다형성에 대한 원칙을 제공&lt;/strong&gt;한다.&lt;/p&gt;

&lt;p&gt;위 원칙을 간단한 코드로 나타내면 아래와 같다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;someMethod&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;SuperClass&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;sc&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;n&quot;&gt;sc&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;someMethod&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;span class=&quot;c1&quot;&gt;//...&lt;/span&gt;

&lt;span class=&quot;n&quot;&gt;someMethod&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;SubClass&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;;&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//정상 동작 해야한다.&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;
&lt;cap&gt;상위 타입의 객체를 사용하는 메서드&lt;/cap&gt;
&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;리스코프-치환-원칙의-위반&quot;&gt;리스코프 치환 원칙의 위반&lt;/h3&gt;

&lt;p&gt;리스코프 치환 원칙은 기능의 명세에 대한 내용이다. 하위 타입이 상위 타입의 기능 명세를 위반했을 때 발생한다.&lt;/p&gt;

&lt;p&gt;그 사례로는 아래와 같은 내용이 있다.&lt;/p&gt;

&lt;ul class=&quot;box-yello&quot;&gt;
  &lt;li&gt;명세에서 벗어난 기능을 수행한다.&lt;/li&gt;
  &lt;li&gt;명세에서 벗어난 값을 리턴한다.&lt;/li&gt;
  &lt;li&gt;명세에서 벗어난 익셉션을 발생한다.&lt;/li&gt;
&lt;/ul&gt;

&lt;h4 id=&quot;명세에서-벗어난-기능을-수행한다&quot;&gt;명세에서 벗어난 기능을 수행한다.&lt;/h4&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Rectangle&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//직사각형&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;width&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;height&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;setWidth&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;width&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;width&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;width&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;setHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;height&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;this&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;height&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;height&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getWidth&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;width&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;height&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt; 
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Square&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;extends&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Rectangle&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//정사각형&lt;/span&gt;
	&lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;setWidth&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;width&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;kd&quot;&gt;super&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;setWidth&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;width&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;kd&quot;&gt;super&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;setHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;width&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	
	&lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;setHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;height&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;kd&quot;&gt;super&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;setWidth&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;height&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;kd&quot;&gt;super&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;setHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;height&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;위 예시는 리스코프 치환 원칙을 설명할때 자주 사용되는 직사각형-정사각형 문제이다.&lt;/p&gt;

&lt;p&gt;Rectangle 클래스는 직사각형을, 그리고 Square 클래스는 Rectangle을 상속받아 정사각형을 구현한다.&lt;/p&gt;

&lt;p&gt;이때, Rectangle의 height를 수정하는 메서드를 살펴보자.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;increaseHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Rectangle&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&amp;lt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getWidth&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;setHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getWidth&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;+&lt;/span&gt; &lt;span class=&quot;mi&quot;&gt;10&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;
&lt;cap&gt;Rectangle의 높이를 조절하는 메서드&lt;/cap&gt;
&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;위 메서드는 직사각형의 높이를 10 높이는 의도를 가지고 있다. 따라서 개발자들은 increaseHeight&lpar;&rpar;의 실행 이후 직사각형은 &lt;strong&gt;서로 다른 width와 height를 지니고 있다고 예상할 것&lt;/strong&gt;이다.&lt;/p&gt;

&lt;p&gt;그러나 increaseHeight의 인자로 &lt;strong&gt;Square 객제가 전달되는 경우 위 가정은 깨지게 되며, increaseHeight&lpar;&rpar;의 의도와 다른 방식으로 동작하게 될 것&lt;/strong&gt;이다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;increaseHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Rectangle&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;instanceof&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Square&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;c1&quot;&gt;// ... 예외 발생&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&amp;lt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getWidth&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;setHeight&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;rec&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getWidth&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;+&lt;/span&gt; &lt;span class=&quot;mi&quot;&gt;10&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;instanceof를 사용한다면 위 문제가 해결될 수 있으나, 앞서 살펴봤듯 Instanceof의 사용은 .그 자체가 개방 폐쇄 원칙을 위반한다.&lt;/p&gt;

&lt;p&gt;위 문제 직사각형과 정사각형이 &lt;red&gt;개념적으로는 상속관계처럼 보이나, 실제로는 그렇지 않기에 발생&lt;/red&gt;한다. 정사각형은 직사각형의 명세에서 벗어난 기능&lpar;가로와 세로폭을 동일하게 고정하는&rpar;을 수행한다.&lt;/p&gt;

&lt;p&gt;따라서 실제 구현에서는 정사각형과 직사각형을 별개의 타입으로 구현해주어야 한다.&lt;/p&gt;

&lt;h4 id=&quot;명세에서-벗어난-값을-리턴한다&quot;&gt;명세에서 벗어난 값을 리턴한다.&lt;/h4&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;CopyUtil&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;copy&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;InputStream&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;is&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OutputStream&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;out&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;kt&quot;&gt;byte&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;byte&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[&lt;/span&gt;&lt;span class=&quot;mi&quot;&gt;512&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;];&lt;/span&gt;
		&lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;len&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;-&lt;/span&gt;&lt;span class=&quot;mi&quot;&gt;1&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
		
		&lt;span class=&quot;c1&quot;&gt;// InputStream의 read 메서드는 스트림의 끝에 도달하면 -1을 반환한다. &lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;while&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;len&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;is&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;read&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;!=&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;-&lt;/span&gt;&lt;span class=&quot;mi&quot;&gt;1&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
			&lt;span class=&quot;n&quot;&gt;out&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;write&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;mi&quot;&gt;0&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;len&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt; 
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;CopyUtil은 InputStream의 &lt;strong&gt;read 메서드는 스트림의 끝에 도달하면 -1을 반환한다&lt;/strong&gt;는 명세를 사용하여 작성된 코드이다.&lt;/p&gt;

&lt;p&gt;이때, InputStream을 상속받는 하위 클래스 SatanInputStream을 아래와 같이 구현했다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;SatanInputStream&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;extends&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;InputStream&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;read&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;kt&quot;&gt;byte&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;mi&quot;&gt;0&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//스트림의 끝에 도달하면 0을 반환&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;만일 개발자가 CopyUtil의 copy 메서드에 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;InputStream&lt;/code&gt; 대신 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;SatanInputStream&lt;/code&gt;을 전달한다면, &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;is.read&lpar;data&rpar;&lt;/code&gt;는 스트림의 끝에서 0을 반환하기에 무한루프를 발생시킨다.&lt;/p&gt;

&lt;p&gt;이는 &lt;strong&gt;하위 클래스 SatanInputStream가 상위 클래스 InputStream의 명세에서 벗어난 값을 리턴했기에 발생하는 문제&lt;/strong&gt;이다.&lt;/p&gt;

&lt;h2 id=&quot;인터페이스-분리-원칙&quot;&gt;인터페이스 분리 원칙&lt;/h2&gt;

&lt;blockquote&gt;
  &lt;p&gt;인터페이스는 그 인터페이스를 사용하는 클라이언트를 기준으로 분리해야 한다. 
&lpar;클라이언트는 자신이 사용하지 않는 메서드에 의존하지 않아야 한다&rpar;&lt;/p&gt;
&lt;/blockquote&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;인터페이스 분리 원칙은 C나 C++과 같이 컴파일과 링크를 직접 해주는 언어를 사용할때 장점이 잘 드러난다.&lt;/p&gt;

&lt;p&gt;그러나 C와 C++에서의 설명은 다른 책이나 포스팅을 찾아보도록 하고, 이 포스팅에서는 Java를 사용하여 설명하도록 하겠다… &lpar;현재 공부하고 있는 책에서는 C로 예시를 들었다.&rpar;&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;interface&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;work&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;eat&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;span class=&quot;c1&quot;&gt;// 사무직 직원&lt;/span&gt;
&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OfficeWorker&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;implements&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;work&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;eat&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;span class=&quot;c1&quot;&gt;// 로봇&lt;/span&gt;
&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Robot&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;implements&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Worker&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;work&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;eat&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;c1&quot;&gt;// 해당 기능이 필요하지 않으나, 인터페이스에 의해 구현해만 한다!&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;위와 코드는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Worker&lt;/code&gt; 인터페이스를 사용하는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OfficeWorker&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Robot&lt;/code&gt;의 예시이다.&lt;/p&gt;

&lt;p&gt;Robot은 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;eat&lpar;&rpar;&lt;/code&gt; 메서드가 필요하지 않으나, Worker 인터페이스를 상속받은 이상 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;eat&lpar;&rpar;&lt;/code&gt; 메서드를 구현해야한다.&lt;/p&gt;

&lt;p&gt;또한 Worker 메서드에 새로운 메서드를 추가한다면, 해당 &lt;strong&gt;인터페이스를 사용하는 클래스 모두에서 변경이 발생&lt;/strong&gt;하게 된다. 해당 메서드가 필요하지 않더라도 말이다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;interface&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Workable&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;work&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;interface&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Eatable&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;eat&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;OfficeWorker&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;implements&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Workable&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;,&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Eatable&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;work&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;eat&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Robot&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;implements&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Workable&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;nd&quot;&gt;@Override&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;work&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;
&lt;cap&gt;인터페이스 분리 원칙이 적용된 코드&lt;/cap&gt;
&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;Worker 인터페이스를 각 클라이언트&lpar;OfficeWorker, Robot&rpar;이 필요로 하는 인터페이스로 분리한다면 위와 같은 문제는 사라진다.&lt;/p&gt;

&lt;p&gt;이렇게 클라이언트 입장에서 사용하는 기능만을 제공하도록 인터페이스의 책임을 분리하는 것은  단일 책임 원칙과도 연결된다. 즉 인터페이스 분리 원칙을 따르는 것으로 &lt;strong&gt;인터페이스와 콘크리트 클래스의 재사용성을 높일 수 있다.&lt;/strong&gt;&lt;/p&gt;

&lt;h2 id=&quot;의존-역전-원칙&quot;&gt;의존 역전 원칙&lt;/h2&gt;

&lt;blockquote&gt;
  &lt;p&gt;고수준 모듈은 저수준 모듈의 구현에 의존해서는 안된다. 
저수준 모듈이 고수준 모듈에서 정의한 추상 타입에 의존해야 한다.&lt;/p&gt;

&lt;/blockquote&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/8ccdb27b-523c-4a5c-8bdb-f5c88e65cb98&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;고수준 모듈과 저수준 모듈은 위와 같이 구분할 수 있다.&lt;/p&gt;

&lt;p&gt;즉, 저수준 모듈은 고수준 모듈에서 사용하는 하위 기능을 실제로 어떻게 구현하는가에 대한 내용을 담고있다.&lt;/p&gt;

&lt;h3 id=&quot;고수준-모듈의-저수준-모듈-의존&quot;&gt;고수준 모듈의 저수준 모듈 의존&lt;/h3&gt;

&lt;p&gt;프로젝트의 초기 요구사항이 안정화된 이후에는, 큰 틀보다는 상세 수준에서의 변경이 주로 발생한다. 따라서 만일 고수준 모듈이 저수준 모듈을 의존하고 있다면, 저수준 모듈의 변경에 따라 고수준 모듈도 함께 변경되게 된다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
13
14
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;caculate&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
	
	&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;someCondition&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;CouponType1&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;type1&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	&lt;span class=&quot;k&quot;&gt;else&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;nc&quot;&gt;CouponType2&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;type2&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
	&lt;span class=&quot;c1&quot;&gt;// Coupon이란 저수준 모듈이 추가될때마다&lt;/span&gt;
	&lt;span class=&quot;c1&quot;&gt;// 고수준 모듈인 가격 계산 모듈이 변경된다.&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;위는 쿠폰의 종류에 따라 가격을 할인해주는 가격 계산 모듈의 예시이다.  이때, 가격 계산 모듈은 개별적인 쿠폰 구현에 의존하고 있다.&lt;/p&gt;

&lt;p&gt;이는 &lt;strong&gt;쿠폰의 구현이 추가되거나 변경될 때마다 가격 계산 모듈의 변경을 야기한다.&lt;/strong&gt;&lt;/p&gt;

&lt;h3 id=&quot;저수준-모듈의-고수준-모듈-의존&quot;&gt;저수준 모듈의 고수준 모듈 의존&lt;/h3&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/dfcee392-707f-46f9-a830-9247fa35e2e9&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;&lt;strong&gt;추상화&lt;/strong&gt;를 사용하면 저수준 모듈이 고수준 모듈을 의존하도록 할 수 있다.&lt;/p&gt;

&lt;p&gt;앞서 살펴봤던 예시인 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;ReservationOrder&lt;/code&gt;의 예시를 살펴보면, 고수준 모듈인 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;DashboardHelper&lt;/code&gt;와 하위 모듈인 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OnlineReservation&lt;/code&gt;과 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;OfflineReservation&lt;/code&gt; 모두 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;ReservationOrder&lt;/code&gt;에 의존하는 것으로 고수준 모듈의 변경 없이 저수준 모듈을 변경할 . 수있는 유연함을 얻을 수 있다.&lt;/p&gt;

&lt;p&gt;이때 만들어지는 ReservationOrder의 인터페이스는 저수준 모듈보다는 고수준 모듈인 DashboardHelper의 입장에서 만들어진다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;interface&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ReservationOrder&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;nc&quot;&gt;Integer&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getTotalPriceOfPaidOrder&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;

	&lt;span class=&quot;nc&quot;&gt;Boolean&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;isMenuAndStatusConfirmed&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;

	&lt;span class=&quot;nc&quot;&gt;Boolean&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;isStatusConfirmedAndPaidWithoutNoShow&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;

	&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;getMenuName&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;
&lt;cap&gt;DashboardHelper의 입장에서 만들어진 ReservationOrder&lt;/cap&gt;
&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;이것은 고수준 모듈이 저수준 모듈에 의존했던 상황이 역전되어, &lt;strong&gt;저수준 모듈이 고수준 모듈이 고수준 모듈에 의존하게 된다는 것&lt;/strong&gt;을 의미한다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;blockquote class=&quot;box-note&quot;&gt;
  &lt;p&gt;저수준 모듈이 고수준 모듈을 의존하도록 변경되었으나, 이는 소스코드상에서의 이야기이지 런타임에서의 의존은 여전히 고수준 모듈의 객체에서 저수준 모듈의 객체로 향한다.&lt;/p&gt;

  &lt;p&gt;런타임에서의 의존과 소스코드의 의존을 구분하도록 하자.&lt;/p&gt;
&lt;/blockquote&gt;
 | 🗓️ 2024/10/01 <br>
 🍙 [디자인패턴&lpar;3&rpar;- 재사용: 상속보단 조립](https://lcqff.github.io/design-pattern-3/) | 👀 &lt;hr /&gt;

&lt;p&gt;이전 포스팅&lt;/p&gt;
&lt;ul&gt;
  &lt;li&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/08/19/design-pattern-1.html&quot;&gt;객체지향&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href=&quot;https://lcqff.github.io/java/2024/09/24/design-pattern-2.html&quot;&gt;다형성과 추상 타입&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;

&lt;hr /&gt;

&lt;h2 id=&quot;개요&quot;&gt;개요&lt;/h2&gt;

&lt;p&gt;객체 지향의 주요 특징 중 하나는 코드의 재사용이다. 이런 재사용을 위해 사용할 수 있는 여러 방법이 있는데, 나는 주로 상속을 사용해왔다.&lt;/p&gt;

&lt;p&gt;그러나 코드를 재사용하기 위해 상속을 사용하는 것은 몇가지 문제점을 초래한다. 이번 챕터에서는 이에 대해 자세히 알아보도록 한다.&lt;/p&gt;

&lt;h2 id=&quot;상속과-재사용&quot;&gt;상속과 재사용&lt;/h2&gt;

&lt;h3 id=&quot;상속&quot;&gt;상속&lt;/h3&gt;

&lt;p&gt;Spring MVC의  Controller 계층구조를 통하여 상속에 대해 알아보자.&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/80db791a-20d0-4653-9849-f7fb3a369f45&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;Spring MVC의 Controller간 상속관계는 위와 같다.&lt;/p&gt;

&lt;p&gt;이때 각 객체는, 자신이 상속받고 있는 상위객체의 기능에 더불어 자신만의 기능을 추가적으로 제공한다.&lt;/p&gt;

&lt;p&gt;이렇게 상속을 상요하면 다른 클래스의 기능을 쉽게 재사용하면서, 추가 기능을 확장할 수 있게된다.&lt;/p&gt;

&lt;p&gt;그러나 상속은 &lt;red&gt;변경의 유연성을 해한다는 치명적인 단점&lt;/red&gt;을 지니고있다.&lt;/p&gt;

&lt;h2 id=&quot;상속을-통한-재사용의-단점&quot;&gt;상속을 통한 재사용의 단점&lt;/h2&gt;

&lt;h3 id=&quot;상위-클래스&quot;&gt;상위 클래스&lt;/h3&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/5f8b273a-3739-47e2-87ba-5f1166a881f3&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;첫번째 포스팅에서 &lt;strong&gt;의존의 전이&lt;/strong&gt;에 대해 다뤘었다.&lt;/p&gt;

&lt;div class=&quot;callout&quot;&gt;
  &lt;div&gt;💡&lt;/div&gt;
  &lt;div&gt;
    &lt;strong&gt;의존&lpar;Dependency&rpar;&lt;/strong&gt;&lt;br /&gt;
    한 객체가 다른 객체를 생성하거나, 파라미터로 전달받거나, 다른 객체의 메서드를 호출하는 것.&lt;br /&gt;
	한 객체의 변경사항이 다른 객체의 변경을 줄 가능성이 높아지는 것.
  &lt;/div&gt;
&lt;/div&gt;

&lt;p&gt;상속또한 다른 객체에 대한 의존을 야기한다. 따라서 의존하는 클래스의 코드의 변경은 해당 클래스를 상속받는 클래스에 또한 변경이 발생할 수 있다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/a601274b-4b77-4400-a5eb-6a875b6e5d90&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;이를태면 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;AbstractController&lt;/code&gt;의 변경은 AbstractController을 상속받은 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;BaseCommandController&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;AbstractUrlViewController&lt;/code&gt;의 변경을 불러일으킬수 있다.&lt;/p&gt;

&lt;p&gt;또한 이렇게 발생한 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;BaseCommandController&lt;/code&gt; 의 변경은 BaseCommandController을 상속받은 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;AbstractCommandController&lt;/code&gt;과 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;AbstractFormController&lt;/code&gt;의 변경을 불러일으킬 수 있다.&lt;/p&gt;

&lt;p&gt;이렇게 상속에 의해 발생한 의존에 의해 변경의 여파는 계층도를 따라 하위 클래스에 계속 전파된다.&lt;/p&gt;

&lt;p&gt;따라서 계층도가 커질수록 상위 클래스의 변경은 점점 어려워진다.&lt;/p&gt;

&lt;h3 id=&quot;클래스의-불필요한-증가&quot;&gt;클래스의 불필요한 증가&lt;/h3&gt;

&lt;p&gt;경우에 따라 상속은 기능 확장에 있어서도 쓰임이 불편할 수 있다.&lt;/p&gt;

&lt;p&gt;아래의 경우를 예시로 들어보자.&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/f7bbfa07-deaa-40b6-80a7-6b7476b5c404&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;위 클래스 계층도는 파일 보관소를 구현한 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Storage&lt;/code&gt; 클래스와, 그에 압축 기능과 암호화 기능을 추가로 구현한 파일 저장소인 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;CompressedStorage&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;EncryptedStorage&lt;/code&gt;이다.&lt;/p&gt;

&lt;p&gt;이제 여기서 기능을 더 확장하려고 한다. 압축을 한 뒤 암호화를 하는 저장소와, 암호화 한 뒤 압축하는 저장소와 암호화된 저장소에 캐시를 적용하는 저장소이다. 상속을 통해 기능을 적용해보자.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/2b952caf-05ed-41a2-afea-d92cfffe8805&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;결과적인 클래스 계층은 위와 같아진다.&lt;/p&gt;

&lt;p&gt;거기에 만일 Java를 사용한다면, 다중상속이 불가능하기에 한개의 클래스만 상속받고 별도로 기능을 구현해주어야 할 것이다.&lt;/p&gt;

&lt;p&gt;이렇게 필요한 기능의 조합이 증가할수록 상속을 통한 기능 재사용은 클래스의 개수 증가를 불러일으킨다.&lt;/p&gt;

&lt;h3 id=&quot;상속의-오용&quot;&gt;상속의 오용&lt;/h3&gt;

&lt;p&gt;상속 자체를 잘못 사용하게 되는 경우또한 발생할 수 있다. 이번에도 예시를 통해 알아보자.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Container&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;extends&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;ArrayList&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;lt;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Luggage&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&amp;gt;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;maxSize&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;int&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;currnetSize&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;put&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Luggage&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;throws&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;NotEnoughSpaceException&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;!&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;canConatain&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&rpar;&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;throw&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;NotEnoughSpaceException&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;kd&quot;&gt;super&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;add&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
		&lt;span class=&quot;n&quot;&gt;currentSize&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;+=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;size&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;ArrayList&lt;/code&gt;를 상속받는 클래스 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Container&lt;/code&gt;가 있다.&lt;/p&gt;

&lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Container&lt;/code&gt; 클래스는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;put&lpar;&rpar;&lt;/code&gt; 메서드를 통해 현재 Container 내부의 크기를 검증하고, 만일 크기가 초과되지 않는다면 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;ArrayList&lt;/code&gt;의 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;add&lpar;&rpar;&lt;/code&gt; 메서드를 통해 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;ArrayList&lt;/code&gt;에 수화물을 추가한 후 Container의 크기를 증가시킨다.&lt;/p&gt;

&lt;p&gt;그러나 위 코드는 아래와 같이 잘못 사용될 수 있다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
11
12
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;nc&quot;&gt;Container&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;c&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Container&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;mi&quot;&gt;5&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;c&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;canContain&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;size3Lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;  
	&lt;span class=&quot;n&quot;&gt;c&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;put&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;size3Lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//정상 사용, currnetSize: 3&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;c&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;canContain&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;size2Lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;n&quot;&gt;c&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;add&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;size2Lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;//비정상 사용, currnetSize 늘어나지 않음.&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;span class=&quot;k&quot;&gt;if&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;c&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;canContain&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;size1Lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;n&quot;&gt;c&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;put&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;size1Lug&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt; &lt;span class=&quot;c1&quot;&gt;// 사이즈 5짜리 컨테이너에 6개의 수화물이 들어갔다!&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;Container 클래스를 개발한 개발자가 다른 개발자들에게 수화물을 추가할때  &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;ArrayList&lt;/code&gt;의 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;add&lpar;&rpar;&lt;/code&gt; 메서드가 아닌 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Container&lt;/code&gt;의 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;put&lpar;&rpar;&lt;/code&gt; 메서드를 사용하라 일렀을지라도, 다른 개발자들은 IDE의 자동완성이 제시한 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;add&lpar;&rpar;&lt;/code&gt; 메서드를 사용할 수 있다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;위와 같은 실수가 발생한 이유는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Container&lt;/code&gt;와 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;ArrayList&lt;/code&gt; 사이에 &lt;red&gt;IS-A 관계가 성립하지 않기 때문&lt;/red&gt;이다.  즉 &lt;strong&gt;Container는 ArrayList가 아니다.&lt;/strong&gt;&lt;/p&gt;

&lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Container&lt;/code&gt;는 수화물을 보관하는 책임을 지는 반면 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;ArrayList&lt;/code&gt;은 목록을 관리하는 책임을 지닌다. 완전히 다른 책임을 지니는 두 클래스를 상속하 문제가 발생하게 된다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;그렇다면 IS-A관계에 해당하지 않는 클래스의 코드를 재사용하기 위해선 무엇을 사용해야하는가?&lt;/p&gt;

&lt;h2 id=&quot;조립을-이용한-재사용&quot;&gt;조립을 이용한 재사용&lt;/h2&gt;

&lt;p&gt;&lt;strong&gt;객체 조립&lpar;Composition&rpar;&lt;/strong&gt;은 여러 객체를 묶어 더 복잡한 기능을 제공하는 객체를 만드는 기술이다.&lt;/p&gt;

&lt;p&gt;객체지향 언어에서 객체 조립은 필드에서 다른 객체를 참조하는 방식으로 구현된다.&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;FlowController&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Encryptor&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;encryptor&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Encryptor&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;process&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;o&quot;&gt;...&lt;/span&gt;
		&lt;span class=&quot;kt&quot;&gt;byte&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;encrtptedData&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;encryptor&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;encrypt&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;data&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;
&lt;cap&gt;객체 참조의 예시&lt;/cap&gt;
&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;클래스-비증식&quot;&gt;클래스 비증식&lt;/h3&gt;

&lt;p&gt;앞서 클래스 증식 문제를 야기한 Storage 예제를 다시 살펴보자.&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/2b952caf-05ed-41a2-afea-d92cfffe8805&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;위와 동일한 기능을 구현하는 객체를 상속이 아닌 객체 조립의 형태로 재구성한다면 아래와 같아진다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/8d8075d6-a9fa-49ab-be0c-936bdcf51298&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;상속 대신 조립을 사용한 객체 Storage는 이제 기능을 확장해도 클래스가 증식하지 않는다. 확장된 기능 또한 조립하면 되기 때문이다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;그렇다면 Storage가 Compressor와 Encryptor을 상속하는 방식으로 구현할수도 있지 않을까?&lt;/p&gt;

&lt;p&gt;그러나 그러한 방식은 Storage 클래스를 저장소 자체가 아닌 압축이나 암호화 목적으로 사용할 수 있게 되며, 경우에 따라 Storage 클래스의 내부 상태가 비정상적으로 변경될 수 있다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;또한 상속의 경우 런타임에서 상위 클래스를 교체할 수 없으나, 조립을 사용하면 런타임시 조립 대상 객체를 교체할 수 있게된다는 장점또한 존재한다.&lt;/p&gt;

&lt;h3 id=&quot;위임&quot;&gt;위임&lt;/h3&gt;

&lt;p&gt;&lt;strong&gt;위임&lpar;delegation&rpar;&lt;/strong&gt;을 통해 내가 할 일을 다른 객체에게 넘길 수 있다. 이는 보통 조립을 사용하여 구현된다.&lt;/p&gt;

&lt;p&gt;아래의 예시를 보자&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;table class=&quot;rouge-table&quot;&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td class=&quot;rouge-gutter gl&quot;&gt;&lt;pre class=&quot;lineno&quot;&gt;1
2
3
4
5
6
7
8
9
10
&lt;/pre&gt;&lt;/td&gt;&lt;td class=&quot;rouge-code&quot;&gt;&lt;pre&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;abstract&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Figure&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Bounds&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;bounds&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;Bounds&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
	
	&lt;span class=&quot;c1&quot;&gt;// ...&lt;/span&gt;
	
	&lt;span class=&quot;kd&quot;&gt;private&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;boolean&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;contains&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;Point&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;point&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
		&lt;span class=&quot;k&quot;&gt;return&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;bounds&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;contains&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;n&quot;&gt;point&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getx&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;,&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;point&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;.&lt;/span&gt;&lt;span class=&quot;na&quot;&gt;getY&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;&rpar;;&lt;/span&gt;
	&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;

&lt;/pre&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;p&gt;위 코드는 마우스 포인터의 위치가 특정 도형이 차지하는 영역에 포함되어 있는지 확인하는 기능을 구현한 코드이다.&lt;/p&gt;

&lt;p&gt;도형과 관련된 클래스 Bounds 클래스가 이미 해당 기능을 제공하고 있기 때문에, 도형을 표현하는 클래스인 Figure 클래스는 Bounds 객체에게 포함 여부 확인을 위임하고 있는 걸 확인할 수 있다.&lt;/p&gt;

&lt;h3 id=&quot;상속은-언제-사용하는가&quot;&gt;상속은 언제 사용하는가?&lt;/h3&gt;

&lt;p&gt;지금까지 상속보다는 조립을 사용한 코드 재사용의 장점을 알아보았다.&lt;/p&gt;

&lt;p&gt;그렇다면 상속은 언제 사용해야 할까?&lt;/p&gt;

&lt;p&gt;상속을 사용할때에는 재사용의 관점이 아닌 &lt;strong&gt;기능의 확장이라는 관점에서 상속을 적용&lt;/strong&gt;해야한다.&lt;/p&gt;

&lt;p&gt;또한 &lt;strong&gt;명확한 IS-A 관계가 성립&lt;/strong&gt;되어야 한다.&lt;/p&gt;

&lt;p&gt;상속을 사용한 클래스 계층은 , 상위 클래스의 기본적인 기능을 그대로 유지하면서 그 기능을 확장해나간다는 특징을 가지고 있다.&lt;/p&gt;
 | 🗓️ 2024/09/30 <br>
 💫 [토익 920점 후기](https://lcqff.github.io/toeic/) | 👀 &lt;p&gt;사실상 자랑에 가까운 게시글이다…. 정보를 위해서 이 글을 읽는 사람은 없길 바란다&lpar;정보성이라곤 전혀 없음&rpar;&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;&lt;img src=&quot;https://github.com/user-attachments/assets/b942c750-0d5f-4264-a7a8-ad82a1e36552&quot; alt=&quot;image&quot; /&gt;&lt;/p&gt;

&lt;p&gt;결론적으로는 목표점수였던 800점을 넘어 920점을 받았다. 이전에 토익을 쳐본적은 없었고, 이번이 첫 시험이었다.&lt;/p&gt;

&lt;h3 id=&quot;기존-영어-실력&quot;&gt;기존 영어 실력&lt;/h3&gt;

&lt;p&gt;솔직히 원래 영어를 못하는 편은 아니다.&lt;/p&gt;

&lt;p&gt;고등학교 때도 영어공부를 필사적으로 하지 않았지만 못하면 3등급, 잘하면 1등급, 일반적으론 2등급 정도가 나왔다. &lpar;절대평가였으니 ‘잘한다’까진 아니고 ‘못하진 않는다’정도로 평가하는게 좋을것 같다.&rpar;&lt;/p&gt;

&lt;p&gt;대학생 2학년 때는 인맥으로 고등학교 야간 교시 아르바이트를 했었다. 3명의 학생에게 영어를 가르쳤다.&lt;/p&gt;

&lt;p&gt;그러나 이 학생들도… 영어를 정말 못하는 아이들이라서 내 실력으로 가르칠 수 있었던 거라 생각한다.&lt;/p&gt;

&lt;p&gt;그러나 이것도 대학년 2학년까지의 이야기… 그 이후로는 영어와는 정말 거리를 두고 살았다. 코딩을 하면서도 정말 간단한 단어의 스펠링을 적을 수 없는 것을 보고 좀 심각하다 느꼈다.&lt;/p&gt;

&lt;p&gt;다시 말해 일단 ‘기초 실력’은 있었다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;그러나 내가 내 영어 실력을 낮게 평가한 것에 비해 기출문제집은 의외로 잘 풀렸다.&lt;/p&gt;

&lt;p&gt;기출문제집을 풀어봤을 때는 시간내에 RC, LC를 포함한 모든 문제를 풀수 있는 실력은 되었다. 굉장히 빈약한… 5분정도의 여유시간이 있었다.&lt;/p&gt;

&lt;p&gt;토익이 점수가 딱딱 정해진 것이 아니라 기출문제집에서 몇점이 나왔다 계산은 할 수 없었지만…&lt;/p&gt;

&lt;p&gt;기출 문제집을 풀어보며 실제 시험에서 아주 못해도 졸업에 필요한 점수는 넘을 거고,  적어도 800점대는 나올거고, 잘하면 900점대가 나올 수도있겠다 생각했다.&lt;/p&gt;

&lt;h3 id=&quot;공부-기간&quot;&gt;공부 기간&lt;/h3&gt;

&lt;p&gt;제대로 공부한것은 4일 정도이다.&lt;/p&gt;

&lt;p&gt;원래는 9월 7일자 시험을 칠 생각이 아니었다. 공부가 더 필요할 것이라 생각했기 때문에…&lt;/p&gt;

&lt;p&gt;그러나 일단 시험이 어떤 느낌으로 진행되는지 알아야 할 것 같아 가장 빠른 시험을 등록했다. &lpar;내 피같은 5만원…&rpar;&lt;/p&gt;

&lt;p&gt;그것이 약 일주일 뒤인 9월 7일의 시험이었다.&lt;/p&gt;

&lt;p&gt;그리고 8월 30일부터 3일까지 여행을 갔다…ㅎㅎ&lt;/p&gt;

&lt;p&gt;총 공부량으로 따지자면 ETS 토익 기출 문제집 RC를 3챕터, LC를 4챕터 풀었다. 문제집에서 나오는 모르는 단어만을 정리했고, 따로 외운 영어 단어는 없다.&lt;/p&gt;

&lt;h3 id=&quot;기출문제집과-실제-시험의-난이도-비교&quot;&gt;기출문제집과 실제 시험의 난이도 비교&lt;/h3&gt;

&lt;p&gt;친구에게는 기출문제집이 실제 시험보다 훨씬 어렵다고 전해들었다. 
LC와 같은 경우 기출문제집보다 훨씬 헷갈렸던거 같다. &lpar;아니면 긴장해서 그랬나…&rpar;&lt;/p&gt;

&lt;p&gt;그러나 RC의 경우 비교적 수훨하게 풀렸던 것 같다.&lt;/p&gt;

&lt;p&gt;풀이 시간과 점수는 기출문제집을 풀었을때와 비슷하게 나왔다. LC가 헷갈렸다고 느껴진 것에 비해 점수는 잘나와서 다행…. 오히려 수월하다 느꼈던 RC가 더 점수가 낮게 나왔다;&lt;/p&gt;

&lt;h3 id=&quot;느낀점&quot;&gt;느낀점&lt;/h3&gt;

&lt;p&gt;900점대가 나와서 기쁘긴한데, 기분이 조금 이상한 것도 사실이다.&lt;/p&gt;

&lt;p&gt;&lpar;물론 920이란 점수가 아주 높은 점수라곤 할 수 없다. 공대 기준 높은 점수이지 문과 기준으로는 900점은 기본으로 받아야 한다 하니까;;&rpar;&lt;/p&gt;

&lt;p&gt;아무튼… 솔직히 지금까지 토익을 좀 두려워해왔던 것도 있다; 이보단 훨씬 어려울줄 알고 계속 미뤄왔던 건데 이렇게 허탈하게 해치울줄은 몰랐다.&lt;/p&gt;

&lt;p&gt;&lpar;물론 내 기대대로 엄청나게 어려운 시험이라서… 700점 이하로 받는것보다 900점을 받는게 낫긴하지만… 그렇긴 하지만…&rpar;&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;p&gt;뭐든 일단 두려워하지 말고 도전을 하자.&lt;/p&gt;

&lt;p&gt;운이 좋다면 내가 두려워했던 것에 비해 별거 아닌 상대일 것이고, 못해도 실전 경험을 얻게되는 것이니 손해볼건 없다.&lt;/p&gt;
 | 🗓️ 2024/09/25 <br><!-- BLOG-POST-LIST:END -->




<!-- 안 쓰는 거-->
<!--README 스탯--> 
<!-- ![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=lcqff&show_icons=true&theme=radical)-->

<!--Git Animals-->
<!--  <a href="https://github.com/devxb/gitanimals">
    <img src="https://render.gitanimals.org/farms/lcqff"/>
  </a> -->

<!--   
  기여도
  [![GitHub Streak](https://streak-stats.demolab.com?user=lcqff&theme=vue&locale=ko&date_format=n%2Fj%5B%2FY%5D)](https://git.io/streak-stats)
    
 가장 많이 사용한 언어
 ![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=lcqff&layout=compact&theme=&hide=html,SCSS,python,c%23,shaderLab)  

  뱃지 (https://github.com/Envoy-VC/awesome-badges)
  ![spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
  ![java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
  ![mysql](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
  ![spring security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=Spring-Security&logoColor=white)
  ![docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
  ![aws](https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)

  
  -->
