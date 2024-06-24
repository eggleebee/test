# 리액트로 포트폴리오 만들기

<ul>
    <li>git init</li>
    <li>git add README.md</li>
    <li>git commit -m "first commit"</li>
    <li>git branch -M main</li>
    <li>git remote add origin https://github.com/eggleebee/test.git</li>
    <li>git push -u origin main</li>
</ul>

<ul>
    <li>Settings</li>
    <li>GitHub Pages
        <ul>
            <li>Pages</li>
            <li>Branch [main]선택</li>
            <li>[save]후 기다리세요</li>
        </ul>
    </li>
    <li>npm i gh-pages</li>
    <li>package.json 파일열고 아래내용추가
        <ul>
            <li>"homepage": "https://eggleebee.github.io/test/",</li>
            <li>"scripts": 
                
                "predeploy": "npm run build",
                "deploy": "gh-pages -d build"
            </li>
        </ul>
    </li>
     <li>npm run deploy</li>
     <li>GitHub Pages
        <ul>
            <li>Pages</li>
            <li>Branch [gh-pages]선택</li>
            <li>[save]후 기다리세요</li>
        </ul>
    </li>
</ul>

build
프로젝트를 한 번 빌드 한 후, gh-pages를 통해 다시 빌드 해준다.

npm run build

npm run deploy

npm run deploy를 통해 npm run build 까지 실행된다고 하지만, 그래도 가장 처음에 npm run build를 해서 build 파일을 만들어줘야 한다.

page 재설정

<em>
“predeploy” : “npm run build”<br/>
npm run deploy 명령어를 입력했을 때 deploy 가 수행되기 전에 build를 한다.<br/>
predeploy는 deploy 전에 먼저 실행한다는 뜻이다. <br/>
이를 통해 build와 deploy를 한번에 실행할 수 있다.
<br/>
“deploy” : gh-pages -d build<br/>
npm run deploy 명령을 수행했을 때 build directory를 배포
</em>
