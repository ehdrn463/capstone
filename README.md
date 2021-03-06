# 경희대학교 2021-1학기 소프트웨어융합캡스톤디자인
## 주제: 그래프 이론 기반 정신질환 증상 점수 네트워크 분석
###       : 정신진단 검사, 임상 증상 평가 척도, 조현병 중증도 비교를 중심으로

------------

결과 위주로 설명드리고, 연구 동기 및 방법론은 하단에 기재하겠습니다.<br>
PPT 슬라이드가 편하신 분은 최하단으로 내리셔서, PPT 참고하시면 됩니다.<br>

------------

### 목차
1. 수행결과
2. 최종결과물 주요특징 및 설명
3. 기대효과 및 활용방안
4. 결론 및 제언
5. 과제 선정 배경 및 필요성
6. 과제 수행 방법
7. PPT 슬라이드

------------

### 1. 수행결과
  - **1) 주관적 정신진단 검사(SCL) - 정신질환 증상(PANSS) Network plot 비교**<br> 
     - Gaussian Graphical Model인 HUGE와 Correlation network 방법인 Spearman, Kendall을 비교했을 때 전체적인 흐름에서 큰 차이가 없었다. 다만 음의 상관관계를 표현하는 edge가 correlation network에서 약해졌다.  
     ![Network_-SCL-PANSS](https://user-images.githubusercontent.com/41279466/123580980-e43c4500-d815-11eb-9d8a-9154175aa67c.jpeg)<br><br>
  - **2) 주관적 정신진단 검사(SCL) - 조현병 중증도 평가(CGI) Network plot 비교**<br> 
     - SCL-PANSS처럼 correlation에 따른 결과에 큰 차이가 없었다. 음의 상관관계가 correlation에서 더 약했다.<br>
     ![Network_-SCL-CGI](https://user-images.githubusercontent.com/41279466/123580979-e3a3ae80-d815-11eb-8af5-85b49293f887.jpeg)<br><br>
  - **3) 주관적 정신진단 검사(SCL) - 정신질환 증상(PANSS) 노드 중심성 Strength 순위**<br> 
     - Strength 척도 기준으로 노드 중심성이 가장 높게 나타난 4개의 변수는 모두 정신질환 증상 (PANSS)였다.<br>  
     <img src="https://user-images.githubusercontent.com/41279466/123580977-e2728180-d815-11eb-9000-0eb46a048534.jpeg" width="50%" /><br><br>
  - **4) 주관적 정신진단 검사(SCL) - 조현병 중증도 평가(CGI) 노드 중심성 Strength 순위**<br> 
     - 주관적 정신진단 검사(SCL)와 조현병 중증도 평가(CGI)에서는 SCL 변수인 ‘긴장감, 우울감, 예민성, 정신분열’이 중요했다.<br>   
     <img src="https://user-images.githubusercontent.com/41279466/123580981-e4d4db80-d815-11eb-870c-a6800a56f785.jpeg" width="50%" /><br><br>
           

------------

### 2. 최종결과물 주요특징 및 설명
Strength 기준으로 노드 중심성이 높게 나온 변수들을 추려 관계를 해석했다.<br>
- **1) 주관적 정신진단 검사(SCL) - 정신질환 증상(PANSS)**<br><br>
   - 가) 의사가 판단한 정신질환 증상 점수인 PANSS는 환자가 기록한 주관적 정신진단 점수인 SCL보다 더 중요한 것으로 드러났다. 일반적인 정신 질환의 경우 ‘환자 본인’의 판단보다 ‘의사’의 판단이 더 중요했다. 약을 처방할 때 PANSS 척도를 더 주의깊게 고려해야 한다.<br>
   - 나) 정신질환 증상(PANSS)에서 음성 반응은 양성 반응, 정신증과 음의 상관관계를 보였다. 음성 반응형 환자와 양성반응 및 정신증형 환자로 나뉘었다. 양·음성 모두 강하게 일어나기보다 유형이 나뉘는 것으로 드러났다.<br>
   - 다) 주관적 정신진단 검사(SCL)의 긴장감은 일반정신병리(PANSS)와 음의 상관관계를 보였다. 그런데 일반정신병리에도 ‘긴장에 대한 설문’이 포함되어 있다. 다른 변수들의 영향력이 ‘긴장’을 상쇄시킨 결과로 보인다.<br>
   - 라) 주관적 정신진단 검사(SCL)의 변수 간에는 전부 양의 상관관계를 보였다. 신체반응, 강박증, 우울증, 불안감, 적대감, 공포불안, 편집증, 대인기피증, 정신분열 증상이 같이 증가하는 경향이 있었다.<br><br>
- **2) 주관적 정신진단 검사(SCL) - 조현병 중증도 평가(CGI)**<br><br> 
   - 가) 의사가 판단한 정신질환 증상 점수인 PANSS는 환자가 기록한 주관적 정신진단 점수인 SCL보다 더 중요한 것으로 드러났다. 그런데 조현병 환자들에게는 의사의 판단인 CGI보다 환자 본인이 판단한 SCL이 더 중요했다. 일반적인 정신질환의 경우엔 의사의 판단이 더 중요했고, 조현병의 경우에는 환자 본인의 판단이 더 중요했다. 약을 처방할 때 조현병 환자 본인이 판단한 점수를 더 주의깊게 고려해야 한다.<br>
   - 나) 조현병 환자의 증상(양·음성 포함)은 공통적으로 주관적 정신진단 검사(SCL)의 우울감과 음의 상관관계를 보였다. 하지만 조현병 양성증상을 보이는 환자에겐 정신분열이 동반됐지만, 음성 증상을 보이는 환자에겐 오히려 정신분열이 줄었다. 즉 모든 변수 간의 관계가 양의 상관관계인 주관적 정신진단 검사(SCL)도 조현병 환자에게는 다른 반응을 보일 수 있다는 것을 시사한다.<br>

------------

### 3. 기대효과 및 활용방안
- **1) 기대효과<br>**
   - 가) 서로 다른 정신질환 증상 점수 간의 관계를 파악하여 표적 치료법 개발에 도움을 줄 수 있다.<br>  
   - 나) 환자의 자가 진단, 의사의 판단의 간극을 좁힐 수 있다.<br> 
   - 다) 일반적인 정신질환 증상의 반응과 다른 조현병 환자에게는 다른 치료법을 적용할 수 있다.<br><br>

- **2) 활용방안<br>**
   - 가) 정신질환 환자의 유형이 양성반응형인지, 음성반응형인지 분석하여 이에 맞는 치료법을 적용하여 예후를 살펴볼 수 있다.<br>
   - 나) 환자가 스스로 생각한 정신질환의 심각도, 의사가 판단한 심각도가 다를 수 있다. 어떤 증상 점수가 더 중요한지 파악해서 그에 맞는 치료가 가능해진다.<br>
   - 다) 조현병 환자이면 일반적인 정신질환의 증상이 무조건 적용되지 않음을 확인했다. 조현병 환자에게는 더 특화된 치료법을 적용한다.<br><br>

------------

### 4. 결론 및 제언
- **1) 결론<br>**
   - 가) Gaussian Graphcial Model을 이용하여 정신질환 증상 평가 간의 관계성을 파악했다. 정신질환 환자 가 양성반응형, 음성반응형으로 나뉘는 것을 확인했다.<br>
   - 나) 환자가 스스로 판단한 정신질환의 심각도와 의사가 진단한 심각도에 차이가 있음을 확인했다.<br>
   - 다) 조현병 환자에게는 일반적인 정신질환 환자와 다른 특화된 치료법을 적용한다.<br><br>

- **2) 제언 및 한계<br>**
   - 가) 전문 의료 인력의 검증을 거친 후, 정신질환 치료법 개발에 적용해야 한다.<br>
   - 나) 정신질환의 종류를 파악하여 그에 맞는 표적 치료법을 개발해야 한다.<br>
   - 다) 분석에 그치지 않고, 의료 인력들이 쉽게 사용할 수 있도록 대쉬보드를 개발해야 한다.<br><br>
     

------------

### 5. 과제 선정 배경 및 필요성
- **1) 정신질환 대처 필요성**<br>
   - 현대인들은 번아웃, 코로나블루를 비롯한 다양한 정신질환에 노출되어 있다. 정신질환은 숨겨야할 부끄러울 질환이었다. 하지만 요즘은 정신질환 환자를 쉽게 찾아볼 수 있을 정도로 감기 같은 질병이 되었다.<br><br>

 - **2) 네트워크 분석 필요성**<br>
   - 정신질환은 같은 병증이어도 다른 증상을 보이기도 한다. 음성 증상은 자연스럽게 일어나야할 행동이나 표현이 과도하게 줄어드는 것이고, 양성 증상은 반대로 더 늘어나는 것이다. 이러한 증상들의 연관성을 파악하는 것은 궁극적으로 병리학적 메커니즘을 이해하여 표적 치료를 개발하는데 도움을 줄 수 있다.<br>

   - 네트워크 분석은 최근 들어 정신의학 집단에서 점점 더 많이 이용되고 있으며, 한 연구에서는 탐색적 요인 분석을 사용한 선행연구의 문제점을 개선하는 데에 쓰이기도 했다. 탐색적 요인 분석을 적용한 연구 결과는 구조를 테스트할 수 있는 수학적 기법이 적용되지 않았으며, 조현병의 음성 증상 구조를 파악하기에 단순하다는 것이었다. 네트워크 분석은 인간, 사회의 관계뿐만 아니라 정신질환의 관계에도 치료법 개발을 위해 이용될 수 있다.<br><br>

------------

### 6. 과제 수행 방법
- **1) R 패키지 과제수행을 위한 도구적 방법**<br>
    - 가) qgraph: weight matrix를 인풋으로 넣어주면 그에 맞는 network plot을 그려주는 R 패키지<br> 
    - 나) High-Dimensional Undirected Graph Estimation (huge): 데이터를 정규성을 띠게 만든 후 partial correlation을 구해주는 R 패키지<br><br>

- **2) 이용된 이론**<br>
    - 가) Graph: node(점), edge(선)로 구성된 요소이다. 방향성이 있으면 directed, 없으면 undirected다. 변수들은 node로, 이들의 관계를 edge로 표현한다. edge는 correlation으로 구하는 것이 일반적이다.<br>
    - 나) Gaussian Graphical Model: 외부변수의 영향력으로 두 변수의 정확한 관계성을 파악하기 힘든 correlation network보다 더 나은 방법이다.<br> 
      - partial correlation을 이용해 두 변수의 정확한 관계를 측정하고, 대규모 데이터셋에도 이용 가능하다.<br>
      - 연구자들이 예측, 이론화하지 못한 관계를 발견할 수 있다.<br>
    - 다) Strength (Centrality 척도 중 하나): 노드의 중요도를 파악하는 방법 중 하나로 가장 직관적이다. 노드에 연결된 다른 노드의 수, 가중치의 합으로 계산된다. 노드들 중에서 다른 노드에 큰 영향력을 미치는 것을 파악할 수 있다.<br>

------------

### 7. PPT 슬라이드
![슬라이드1](https://user-images.githubusercontent.com/41279466/123584086-b8bc5900-d81b-11eb-963d-f5843103ae68.JPG)
![슬라이드2](https://user-images.githubusercontent.com/41279466/123584090-b9ed8600-d81b-11eb-90a3-26a63b6d1a7b.JPG)
![슬라이드3](https://user-images.githubusercontent.com/41279466/123584091-ba861c80-d81b-11eb-989b-5c533c294115.JPG)
![슬라이드4](https://user-images.githubusercontent.com/41279466/123584092-ba861c80-d81b-11eb-9ef0-ab0d6801257b.JPG)
![슬라이드5](https://user-images.githubusercontent.com/41279466/123584095-bb1eb300-d81b-11eb-94b1-7d8a03f96b5c.JPG)
![슬라이드6](https://user-images.githubusercontent.com/41279466/123584097-bbb74980-d81b-11eb-89b6-c16baa64c4dd.JPG)
![슬라이드7](https://user-images.githubusercontent.com/41279466/123584098-bbb74980-d81b-11eb-965c-fa42222e9d35.JPG)
![슬라이드8](https://user-images.githubusercontent.com/41279466/123584099-bc4fe000-d81b-11eb-9106-7282e30636ae.JPG)
![슬라이드9](https://user-images.githubusercontent.com/41279466/123584100-bc4fe000-d81b-11eb-9ad9-6298d05bbffe.JPG)
![슬라이드10](https://user-images.githubusercontent.com/41279466/123584103-bce87680-d81b-11eb-9531-4232fc546981.JPG)
![슬라이드11](https://user-images.githubusercontent.com/41279466/123584105-bce87680-d81b-11eb-86a2-b668a3ca7f2b.JPG)
![슬라이드12](https://user-images.githubusercontent.com/41279466/123584107-bd810d00-d81b-11eb-8c80-4c2fbc1a6a6a.JPG)
![슬라이드13](https://user-images.githubusercontent.com/41279466/123584108-be19a380-d81b-11eb-9ee0-ad0c6eab28b3.JPG)
![슬라이드14](https://user-images.githubusercontent.com/41279466/123584110-be19a380-d81b-11eb-821b-4bf39720dac0.JPG)
![슬라이드15](https://user-images.githubusercontent.com/41279466/123584111-beb23a00-d81b-11eb-8246-56d4b0ace5bb.JPG)
![슬라이드16](https://user-images.githubusercontent.com/41279466/123584112-beb23a00-d81b-11eb-91fb-b7fb5bd1c668.JPG)
![슬라이드17](https://user-images.githubusercontent.com/41279466/123584113-bf4ad080-d81b-11eb-934c-e3ebd4b00e82.JPG)
![슬라이드18](https://user-images.githubusercontent.com/41279466/123584115-bfe36700-d81b-11eb-8af6-5f6d475c95ae.JPG)
![슬라이드19](https://user-images.githubusercontent.com/41279466/123584116-bfe36700-d81b-11eb-8e7f-13d1bbf5b1b6.JPG)
![슬라이드20](https://user-images.githubusercontent.com/41279466/123584117-c07bfd80-d81b-11eb-9cd8-49e94d98155f.JPG)
![슬라이드21](https://user-images.githubusercontent.com/41279466/123584118-c07bfd80-d81b-11eb-8b2a-f9941e0fb197.JPG)
![슬라이드22](https://user-images.githubusercontent.com/41279466/123584119-c1149400-d81b-11eb-9222-d6938b981d15.JPG)


