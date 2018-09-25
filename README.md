# AR.js 관련 레퍼런스



## 테스트 페이지

**https://ar-test.colaboapp.cc/ar-test/**



## 관련 링크

링크: **https://aframe.io/blog/arjs/**


- 웹 기반 마커 기반 AR 기술
- 3D 모델 파일 포맷: .gltf
- 마커 파일 포맷: .patt
- A-Frame 과 엮어서 사용함.



## AR.js 관련 문서

링크: **https://aframe.io/**

### 기본 구조

```HTML
<!-- A-Frame과 AR.js 관련 소스 추가 -->
<script src="https://aframe.io/releases/0.6.0/aframe.min.js"></script>
<script src="https://jeromeetienne.github.io/AR.js/aframe/build/aframe-ar.js"></script>

<!--바디 부분-->
<body style='margin : 0px; overflow: hidden;'>
	<!--a-scene 태그를 사용하여 AR.js 로드-->
    <a-scene embedded arjs>
        
    <!-- :: AR로 띄울 대상 쓰는 부분 :: -->
    <a-box position='0 0.5 0' material='opacity: 0.5;'></a-box>
    <!-- :: :: -->
        
    <!-- 카메라가 어떠한 마커를 기준으로 움직일지를 쓰는 부분 -->
    <a-marker-camera preset='hiro'></a-marker-camera>
  </a-scene>
</body>
```



### AR 대상 띄우는 부분

```HTML
	<!-- :: AR로 띄울 대상 쓰는 부분 :: -->
	
```









## GLTF  관련 문서

- https://www.khronos.org/gltf/

- 위 문서에서 **일반 3D 파일에서 gltf파일로 변환이 가능한 툴들을 제공**하고 있음.



## PATT 관련 문서

- 