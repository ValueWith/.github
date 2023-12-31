## 일정 등록

![T일정등록](https://github.com/ValueWith/.github/assets/110911811/7674c389-71f8-4691-9fdc-9c8d17fe34b7)
![T장소등록](https://github.com/ValueWith/.github/assets/110911811/c7d0117b-9dd8-4c1d-b93d-346fcec6f337)

### Frontend

```
✅ 검색 데이터 / 추천 데이터 등록

카카오 로컬 API 에서 검색어 장소 데이터를 최대 45개까지 받아옵니다.
장소 추천받기를 클릭하면 TourAPI에서 지역별로 장소 데이터를 받아옵니다.
이렇게 불러온 데이터는 인피니티 스크롤(Infinity Scroll)을 활용하여 사용자에게 보여줍니다.
```

```
✅ 카카오맵을 활용한 다양한 기능 구현

사용자가 장소를 선택하면 해당 장소의 중심 위치로 지도가 이동합니다.

카카오맵에 일정 순서 커스텀 마커를 생성하고 각 마커 사이에 Polyline을 그려 한 눈에 경로를 파악할 수 있도록 하였습니다.

일정을 등록하고 순서를 바꿀 수 있도록 드래그 앤 드랍 기능을 제공합니다.
순서가 바뀔 경우 카카오맵의 순서와 Polyline을 재배치합니다.
```

```
✅ react-hook-form을 이용한 폼 유효성 검사

react-hook-form은 비제어 컴포넌트를 활용하여 불필요한 리렌더링을 방지하여 직접 구현할 때보다 성능상 이점이 있고, 실시간 유효성 검사 등 다양한 기능을 제공합니다.
Tweaver는 react-hook-form에서 제공하는 다양한 훅을 활용하여 폼의 상태를 검증하고 있습니다.
```

### Backend

```
✅ 경로의 경도, 위도, 주소, 장소Code, 순서, 거리를 각 일정에 등록
```

```
✅ 카카오 모빌리티 자동차 길찾기 API

각 경로 사이의 거리를 카카오 모빌리티 자동차 길찾기 API를 활용하여 단순 좌표 사이의 직선거리가 아닌 실제 이동거리로 계산하여, 사용자에게 보다 최적화된 정보를 제공합니다.
길찾기 API에서 찾아낸 각 경로 사이의 거리를 Place테이블 distance필드에 저장합니다.
```

```
✅ 추천 경로 구현 (카카오 모빌리티 다중 목적지 API + 완전 탐색 알고리즘)

등록한 일정의 동선이 최적이 되는 경로를 추천받고 싶은 경우를 위한 기능으로,
카카오 모빌리티 API에서 받아온 좌표 사이의 거리를 최단 경로 순서로 배열합니다.
```
