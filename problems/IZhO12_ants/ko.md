$K$마리의 개미가 큰 마당을 돌아다니고 있습니다. 마당은 $W \times H$ 크기의 직사각형 모양이며 한 꼭지점은 $(0, 0)$에 있고 마주보는 꼭지점은 $(W, H)$에 있습니다. 각 개미는 4방위(동서남북) 중 한 방향으로 1초에 1cm씩 움직일 수 있습니다.

개미들은 매우 오만한(?) 생물이기에, 절대 양보하지 않습니다. 따라서, 여러 마리의 개미들이 마주보는 방향에서 만나게 되면, 그들은 즉시 뒤돌아서 반대 방향으로 전진합니다. 만약 두 개미가 수직하게 만난다면 그들은 서로 신경쓰지 않을 것입니다. 개미가 마당의 네 변에 닿아도 뒤돌아서 반대 방향으로 이동합니다.

개미들의 초기 위치와 방향이 주어질 때, $T$초가 지나면 각각 어느 위치에 있고 어느 방향으로 이동하고 있는지 계산하는 프로그램을 작성하세요.

### 입력 형식

첫 번째 줄에는 4개의 정수 $W, H, K, T$ ($1 \le W, H, K \le 100, 1 \le T \le 10^{9}$)

다음 $K$개 줄에는 각각 3개의 정수 $X_{i}, Y_{i}, D_{i}$입니다. $(X_{i}, Y_{i})$는 개미의 초기 위치이고, $D_{i}$는 개미가 이동하는 방향입니다. ($0 < X_{i} < W, 0 < Y_{i} < H, 1 \le D_{i} \le 4$) 만약 개미가 $x$좌표가 증가하는 방향으로 이동하면 $D_{i}=1$, $y$좌표가 증가하는 방향으로 이동하면 $D_{i}=2$, $x$좌표가 감소하는 방향으로 이동하면 $D_{i}=3$, $y$좌표가 감소하는 방향으로 이동하면 $D_{i}=4$입니다.

주어지는 모든 수들은 공백으로 구분되어 있고, 모든 개미들은 서로 다른 위치에 있습니다.

### 출력 형식

정확히 $K$줄을 출력합니다. 각 줄에는 개미가 $T$초 뒤에 위치한 $x$좌표와 $y$좌표, 그리고 이동 방향을 공백으로 구분하여 출력해야 합니다. 방향은 입력 형식을 따릅니다.

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">4 4 2 3<br/>
1 1 1<br/>
3 3 4</td>
   <td class="code-font">4 1 3<br/>
3 0 2</td>
  </tr>
  <tr>
   <td class="code-font">4 4 2 4<br/>
1 1 1<br/>
3 3 4</td>
   <td class="code-font">3 1 3<br/>
3 1 2</td>
  </tr>
  <tr>
   <td class="code-font">4 4 2 2<br/>
1 1 1<br/>
3 1 3</td>
   <td class="code-font">1 1 3<br/>
3 1 1</td>
  </tr>
  <tr>
   <td class="code-font">4 4 2 2<br/>
2 1 1<br/>
3 1 3</td>
   <td class="code-font">1 1 3<br/>
4 1 3</td>
  </tr>
 </tbody>
</table>

### 참고

60%의 테스트 케이스에 대해 $1 \le T \le 1,000.$