Transactional
=============
>@Transactional : 테스트 케이스에 이 애노테이션이 있으면, 테스트 시작 전에 트랜잭션을 시작하고,
테스트 완료 후에 항상 롤백한다. 이렇게 하면 DB에 데이터가 남지 않으므로 다음 테스트에 영향을 주지
않는다.



test에서 @Transactional을 사용하면 트랜젝션이 먼저 실행되며
테스트에서 사용한 코드는 다시 롤백을 해준다.

테스트 시 사용됨.(각각의 테스트마다 실행된다.)

반복적인 테스트가 가능하다.