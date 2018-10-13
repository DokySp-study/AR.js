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

```html
<a-scene embedded arjs>
    
    <!--여기에 오브젝트로 띄울 아이템 배치-->
    <!-- <a-assets>: 오브젝트를 에셋으로 설정할 때 주로 씀 -->
    <!-- <a-entity>: 실제 에셋을 이용하여 오브젝트를 공간에 배치 -->
    
    <a-marker-camera type="pattern" url="패턴파일(.patt) 경로"></a-marker-camera>
</a-scene>
```

#### 예시

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

- **OBJ(3D Model):** https://aframe.io/docs/0.8.0/components/geometry.html
  - obj 파일과 옵션으로 mtl 파일을 지원함.
- **GLTF(3D Ani Model):** https://aframe.io/docs/0.8.0/components/gltf-model.html#sidebar
- **Image:** https://aframe.io/docs/0.8.0/primitives/a-image.html#sidebar
- **Video:** https://aframe.io/docs/0.8.0/primitives/a-video.html#sidebar
  - 모바일의 경우, 비디오 자동재생이 되지 않는 문제가 있음.
- **Video Croma Key**: 
  - 모바일의 경우, 비디오 자동재생이 되지 않는 문제가 있음.



#### 2-1. 미디어 앨리먼트

- scale: https://aframe.io/docs/0.8.0/components/scale.html#sidebar
- rotation: https://aframe.io/docs/0.8.0/components/rotation.html#sidebar
- position: https://aframe.io/docs/0.8.0/components/position.html#sidebar



___

### 3. 인식 패턴(PATT) 수정 <!!>

- 패턴 만들기: https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html
- 패턴 수정: 상단의 코드 참조
- 패턴 만들기: **패턴 인식 범위가 16x16**이므로 **백색 바탕에 알파벳 한 글자 정도**가 인식률이 높다.





## GLTF  관련 문서

- https://www.khronos.org/gltf/
- 위 문서에서 **일반 3D 파일에서 gltf파일로 변환이 가능한 툴들을 제공**하고 있음.



## Project Route 연계

- 마커 생성은 링크만 안내하고, patt 파일을 홈페이지에서 읽을 수 있도록 해야 할 듯
- 3D Animation은 fbx파일 또는 gltf파일을 사용해야 하는데 테스트가 잘 안됨..
- Youtube를 사용한 실시간 AR랜더링이 가능한지 테스트 해보았지만, AR.js가 iframe 지원을 안하는듯..
  - 따라서 입체 모형을 만들고 쉐이더에 씌우는 방법이 있긴 한데 아직 테스트중.
- iOS에서 권한 문제로 동영상과 크로마키 동영상이 재생이 힘든 부분이 있음.