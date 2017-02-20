IOI 2015 개막식이 거의 끝나가고 있다. 개막식이 진행되는 동안, 각 팀은 주최측으로부터 선물상자를 받게 되어 있다. 그러나 모든 자원봉사자들이 개막식에 너무 집중하는 바람에, 선물에 대해서는 완전히 잊고 있었다. 선물을 줘야 한다는 것을 기억하는 사람은 아만 뿐이다. 아만은 열정적인 자원봉사자이며, IOI가 완벽하게 진행되었으면 하는 바램으로 모든 선물을 최소의 시간에 전달하고자 한다.

개막식이 진행되는 곳은 L개의 동일한 구역으로 나뉘어진 원 모양이다. 각 구역은 차례로 0부터 L-1까지 번호가 매겨져 있다. 즉, 0 ≤ i ≤ L-2일 때, 구역 i와 구역 i+1는 서로 인접해 있고, 구역 0과 구역 L-1도 서로 인접해 있다. 개막식에 온 팀들은 모두 N개 팀이다. 각 팀은 이 구역들 중 하나에 앉아 있다. 각 구역에는 임의의 수의 팀들이 있을 수 있다. 어떤 구역에는 팀이 전혀 없을 수도 있다.

선물은 모두 동일하며, 총 N개가 있다. 처음에, 아만과 모든 선물은 구역 0에 있다. 아만은 각 팀에게 선물을 하나씩 주어야 하며, 선물을 다 나눠준 다음에는 구역 0으로 돌아와야 한다. 구역 0에도 팀들이 있을 수 있음에 주의하자.

어떤 순간에도, 아만은 최대 K개의 선물들만을 들 수 있다. 아만은 구역 0에서 선물을 들어야 하고, 드는데는 시간이 들지 않는다. 각각의 선물은 팀에게 전달될 때까지 아만이 들고 있어야 한다. 아만이 하나 이상의 선물을 들고 있고, 아직 선물을 받지 않은 팀(들)이 있는 구역에 도착하면, 아만은 들고 있는 선물을 팀(들)에게 줄 수 있다. 선물을 주는데도 시간이 들지 않는다. 시간이 드는 것은 단지 이동 뿐이다. 아만은 원형인 개막식장에서 양 방향으로 움직일 수 있다. 인접한 구역간을 이동하는데 (시계방향이든 반시계방향이든) 정확히 1초가 걸리며, 선물을 몇 개 들고 있는지와는 관계가 없다.

아만이 모든 선물을 전달하고, 처음 위치로 돌아오는데 필요한 최소의 시간을 구하시오.

### 예제

이 예제에서 N = 3팀이 있고, 아만은 동시에 최대 K = 2개의 선물을 들 수 있으며, 구역의 수는 L = 8이다. 팀들은 구역 1, 2, 5에 있다.

<div style="text-align: center;">
<img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/IOI15_boxes/1.png" style="max-width: 720px;"/>
</div>

최적의 해 중 하나가 위 그림에 나와 있다. 처음에 아만은 선물 두 개를 들고, 이를 구역 2에 있는 팀에게 하나를 전달하고, 나머지 하나를 구역 5에 있는 팀에게 준 뒤 구역 0으로 돌아온다. 이 과정은 8초가 걸린다. 다음에 아만은 남은 선물 하나를 구역 1에 있는 팀에게 주고 다시 구역 0으로 돌아온다. 이 과정은 2초가 걸린다. 따라서, 전체 시간은 10초이다.


### 문제

N, K, L과 모든 팀들의 위치가 주어진다. 아만이 모든 선물을 전달하고 구역 으로 돌아오는데 걸리는 시간의 최소값을 구하시오.

이를 위하여 `delivery` 함수를 구현해야 한다:

* `delivery(N, K, L, positions)`
 * `N`: 팀의 수
 * `K`: 아만이 한 번에 들 수 있는 선물의 최대 개수 
 * `L`: 개막식장의 구역 수
 * `positions`: 길이 N인 배열. `positions[0], ..., positions[N-1]`에 각 팀이 있는 구역 번호가 주어진다. `positions`의 성분들은 감소하지 않는 순서로 주어진다.

이 함수의 리턴값은 아만이 임무를 완수하는데 최소 몇 초가 필요한지이다.


### Sample grader

**Sample grader는 [여기](https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/IOI15_boxes/graders.zip)에서 다운로드할 수 있습니다.** 

Sample grader는 다음 양식에 따라 입력을 읽어들인다.

* line 1 : `N K L`
* line 2 : `positions[0] ... positions[N-1]`

Sample grader는 `delivery`의 리턴 값을 출력한다.