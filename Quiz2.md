# 1. B 트리 최적화 중에 해당되지 않는 것은?

1. 페이지 덮어 쓰기와 고장 복구를 위한 WAL 유지 대신 (LMDB 같은) 일부 데이터베이스는 쓰기 시 복사 방식(copy-on-write scheme)을 사용
2. 페이지에 전체 키를 저장하는 게 아니라 키를 축약해 쓰면 공간을 절약
3. 많은 B 트리 구현에서 루트(root) 페이지를 디스크 상에 연속된 순서로 나타나게끔 트리를 배치하려 시도
4. 트리에 포인터를 추가

# 2. 색인과 관련된 것 중 틀린 것은?
1. 색인에서 키는 질의가 검색하는 대상이지만 값은 다음의 두 가지 중 하나는 다른 곳에 저장된 로우를 가리키는 참조이다. 이때 저장된 곳을 **힙 파일** 이라 한다
2. 어떤 상황에서는 색인 안에 바로 색인된 로우를 저장하는 편이 바람직하다. 이를 **클러스터드 색인(clustered index)** 이라 한다
3. 다중 칼럼 색인의 가장 일반적인 유형은 **결합 색인** 이다. 하지만 지리 공간 데이터 같은 2개의 필드 범위 질의에 어울리지 않는다
4. 루씬에서 인메모리 색인은 여러 키 내 문자에 대한 유한 상태 오토마톤 **트라이(trie)** 와 유사하다
