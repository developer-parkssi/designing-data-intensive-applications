# 고전적인 데이터베이스 교과서에서는 격리성을 "직렬성"이라는 용어로 공식화한다. 여기에서 "직렬성"이 데이터베이스에서 무엇을 의미하는지 설명하시오
- 직렬성은 각 트랜잭션이 전체 데이터베이스에서 실행되는 유일한 트랜잭션인 것처 럼 동작할 수 있다는 것을 의미
- 데이터베이스는 실제로는 여러 트랜잭션이 동시에 실행됐더라 도 트랜잭션이 커밋됐을 때의 결과가 트랜잭션이 **순차적으로**(하나씩 차례로) 실행됐을 때의 결과와 동일하도록 보장

# 커밋 후 읽기를 하다보면 일시적인 비일관성을 감내할 수 없는 경우도 있다고한다. 그래서 "스냅숏 격리"가 이런 문제의 가장 흔한 해결책이라고 하는데 어떤 경우가 있고 간단히 설명하시오
- 백업
- 분석 질의의 무결성 확인
