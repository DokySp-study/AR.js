# AR.js 관련 레퍼런스



## 테스트 페이지

**https://ar-test.colaboapp.cc/**



## 관련 링크

링크: **https://aframe.io/blog/arjs/**


- 웹 기반 마커 기반 AR 기술
- 3D 모델 파일 포맷: .gltf (.obj도 지원)
- 마커 파일 포맷: .patt
- A-FRAME 과 엮어서 사용함.



## AR.js 관련 문서

링크: **https://aframe.io/**

### 1. 기본 구조

```HTML
<!-- A-Frame과 AR.js 관련 소스 추가 -->
<script src="https://aframe.io/releases/0.6.0/aframe.min.js"></script>
<script src="https://jeromeetienne.github.io/AR.js/aframe/build/aframe-ar.js"></script>

<!--바디 부분-->
<body style='margin : 0px; overflow: hidden;'>
	<!--a-scene 태그를 사용하여 AR.js 로드-->
    <a-scene embedded arjs>
        
        
    <!-- :: AR 미디어 띄우는 부분 :: -->
    <a-box position='0 0.5 0' material='opacity: 0.5;'></a-box>
    <!-- :: :: -->
        
        
    <!-- !! 마커 및 카메라 설정 부분 !! -->
    <!--<a-marker-camera preset='hiro'></a-marker-camera>-->
    <a-marker-camera type='pattern' url='path/to/pattern-marker.patt'></a-marker-camera>
    <!-- !! !! -->

  </a-scene>
</body>
```

___

### 2. AR 미디어 <::>

 ` A-FRAME이 지원하는 미디어 유형을 모두 사용할 수 있다`

- **OBJ:** https://aframe.io/docs/0.8.0/components/geometry.html
  - obj 파일과 옵션으로 mtl 파일을 지원함.
- **GLTF:** https://aframe.io/docs/0.8.0/components/gltf-model.html#sidebar
- **Image:** https://aframe.io/docs/0.8.0/primitives/a-image.html#sidebar
- **Video:** https://aframe.io/docs/0.8.0/primitives/a-video.html#sidebar
  - 모바일의 경우, 비디오 자동재생이 되지 않는 문제가 있음.



#### 2-1. 미디어 앨리먼트

- scale: https://aframe.io/docs/0.8.0/components/scale.html#sidebar
- rotation: https://aframe.io/docs/0.8.0/components/rotation.html#sidebar
- position: https://aframe.io/docs/0.8.0/components/position.html#sidebar



___

### 3. 인식 패턴(PATT) 수정 <!!>

- 패턴 만들기: https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html
- 패턴 수정: 상단의 코드 참조





## GLTF  관련 문서

- https://www.khronos.org/gltf/

- 위 문서에서 **일반 3D 파일에서 gltf파일로 변환이 가능한 툴들을 제공**하고 있음.
