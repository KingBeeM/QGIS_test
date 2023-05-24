# QGIS_test

## Python 주요 라이브러리
- geopandas
  + DataFrame + 지리공간데이터
- Shapely
  + 점, 선, 다각형(polygon) 등의 2D 기하 도형객체를 조작(handling)
- PyProj
  + 지리좌표계와 투영좌표계간 변환
- Rasterio
  + 위성이미지 저장, 불러오기 numpy 변환 등


## Domain 지식
- Raster
  + 셀 또는 픽셀 그리드 표현
  + 위성 이미지, 항공사진 등의 시각화
  + 고도(Elevation, 온도)
- Vector
  + 점, 선, 다각형 특징
  + 빌딩의 경계, 호수, 강 등
  + 지구의 표면적인 특징
  + 빌딩의 정보, 주소, 가격, 건축 날짜 등의 정보를 Polygon 형태에 저장을 시킬 수 있음
    * Polygon : 각각의 좌표의 개별적인 성질 특성 등을 담을 수 있다.

## Shapefile
- 지리 공간 벡터 데이터의 파일 형태
- 세가지 파일 형태(.shp, .shx, .dbf)
  + .shp : vector geometry (점, 선, 다각형)
  + .shx : index file, .shp 파일에 빠르게 접근 할 수 있도록 도와주는 역할
  + .dbf : 각 vector 피처들의 속성 정보들이 포함

## CRS(Coordinate Reference System)
- 좌표 체계 : 위도, 경도
- 세가지 유형
  + GCS(Geographic Coordinate Systems)
    * 위도 및 경도 좌표(WGS84, NAD83)
  + PCS(Projected Coordinate Systems)
    * 투영 좌표계 : 곡면을 표면으로 변환하는 과정에서 생기는 거리, 방향, 면적의 왜곡이 발생
  + VCS(Vertical Coordinate Systems)
    * 해양과학, 해수면 등과 관련
