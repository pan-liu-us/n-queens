# n-queens
This is a project I completed as a student at [hackreactor](http://hackreactor.com). This project was worked on with a pair.

<div>
  <h2 id="the-problem-in-a-nutshell">The problem in a nutshell</h2>
  <p>Given an <em>n x n</em> chessboard, how many different ways can you place <em>n</em> queens, such that none of them are attacking each other?</p>
  <h2 id="for-your-consideration">For your consideration</h2>
  <p>Pondering the following questions (in order) will help you conceptualize a solution:</p>
  <ul class="task-list">
    <li class="task-list-item"><input type="checkbox" class="md-task"> Given an <em>n x n</em> chessboard, how would you place <em>n</em> rooks such that none of them are attacking each other?</li>
    <li class="task-list-item"><input type="checkbox" class="md-task"> Given an <em>n x n</em> chessboard, how many different ways can you place <em>n</em> rooks, such that none of them are attacking each other?</li>
    <li class="task-list-item"><input type="checkbox" class="md-task"> Given an <em>n x n</em> chessboard, how would you place <em>n</em> queens such that none of them are attacking each other?</li>
    <li class="task-list-item"><input type="checkbox" class="md-task"> Given an <em>n x n</em> chessboard, how many different ways can you place <em>n</em> queens, such that none of them are attacking each other?</li>
  </ul>
  <p>You'll run into some questions like this (but easier) during some interviews, and during your day-to-day work. This repo is a playground for thinking about this kind of problem.</p>
  <h2 id="helpful-groundwork">Helpful Groundwork</h2>
  <p>To get started, we've provided a visualizer for your algorithms. Most algorithm questions are posed abstractly, but this Backbone app will help you see what's going on inside your code more easily.</p>
  <p>To make use of it, run <code tabindex="0">npm start</code> and navigate to <code tabindex="0">BoardViewer.html</code>. You'll be implementing the conflict detection functions in <code tabindex="0">src/Board.js</code> as stepping stones to your solution.</p>
  <h2 id="bare-minimum-requirements">Bare Minimum Requirements</h2>
  <p><em>(Read this section and the Helpful Info section before beginning. After completing the bare minimum requirements, proceed to the Advanced content section.)</em></p>
  <p>Some of the helper functions in <code tabindex="0">src/Board.js</code> have been completed for you, and some have not. You should only need to edit the functions listed below.</p>
  <ul class="task-list">
    <li class="task-list-item">
      <p><input type="checkbox" class="md-task"> Open <code tabindex="0">src/Board.js</code> and fix the incomplete helpers (look for the 'start here' section) such that the specs in <code tabindex="0">spec/BoardSpec.js</code> pass. To see if your specs are passing, run <code tabindex="0">npm start</code> and navigate to <code tabindex="0">SpecRunnner.html</code> and look at the 'Board' section. Doing so will help you understand the problem more thoroughly, and will make the visualizer show any conflicts on the board.</p>
      <ul class="task-list">
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>hasRowConflictAt()</strong>: test if a specific row on this board contains a conflict</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>hasAnyRowConflicts()</strong>: test if any rows on this board contain a conflict</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>hasColConflictAt()</strong>: test if a specific column on this board contains a conflict</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>hasAnyColConflicts()</strong>: test if any columns on this board contain a conflict</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>hasMajorDiagonalConflictAt()</strong>: test if a specific major diagonal on this board contains a conflict</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>hasAnyMajorDiagonalConflicts()</strong>: test if any major diagonals on this board contain a conflict</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>hasMinorDiagonalConflictAt()</strong>: test if a specific minor diagonal on this board contains a conflict</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>hasAnyMinorDiagonalConflicts()</strong>: test if any minor diagonals on this board contain a conflict</li>
      </ul>
    </li>
    <li class="task-list-item">
      <p><input type="checkbox" class="md-task"> Fill in the functions in <code tabindex="0">src/solvers.js</code>. Fill them out so they accomplish the stated goals and pass the tests in <code tabindex="0">spec/solversSpec.js</code></p>
      <ul class="task-list">
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>findNRooksSolution()</strong>: returns a single solution to the n-rooks problem</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>countNRooksSolutions()</strong>: returns a count of the total number of solutions to the n-rooks problem</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>findNQueensSolution()</strong>: returns a single solution to the n-queens problem</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> <strong>countNQueensSolutions()</strong>: returns a count of the total number of solutions to the n-queens problem</li>
      </ul>
    </li>
    <li class="task-list-item">
      <p><input type="checkbox" class="md-task"> Identify the time complexity of each of your helper methods, as well as for each of your working solutions</p>
    </li>
  </ul>
  <h2 id="helpful-info">Helpful Info</h2>
  <ul>
    <li>
      <p>Don't reinvent the wheel where you don't have to. Use the Board constructor you build out in <code tabindex="0">src/Board.js</code> in your code. You can also access it within the Chrome console easily after opening <code tabindex="0">BoardViewer.html</code></p>
      <ul>
        <li>Create new board instances that have access to all the helper methods you write in <code tabindex="0">src/Board.js</code>
          <ul>
            <li>example: <code tabindex="0">var board = new Board({n:5})</code></li>
          </ul>
        </li>
        <li>Rather than setting or getting object properties directly with plain JavaScript, Backbone provides the <code tabindex="0">get</code> and <code tabindex="0">set</code> methods. Play with the getters and setters that Backbone provides
          <ul>
            <li>example: <code tabindex="0">board.get(3)</code> will return the 3rd row of the instance <code tabindex="0">board</code> (assuming that instance exists)</li>
          </ul>
        </li>
      </ul>
    </li>
    <li>
      <p><strong>Rows</strong> run horizontally, left to right</p>
    </li>
    <li>
      <p><strong>Columns</strong> run vertically, top to bottom</p>
    </li>
    <li>
      <p><strong>Major Diagonals</strong> run diagonally, top-left to bottom-right</p>
    </li>
    <li>
      <p><strong>Minor Diagonals</strong> run diagonally, top-right to bottom-left</p>
    </li>
    <li>
      <p>In <a href="https://en.wikipedia.org/wiki/Chess" class="external-link" target="_blank">chess
          <svg class="svg">
            <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
          </svg>
        </a> the <a href="https://en.wikipedia.org/wiki/Rook_(chess)" class="external-link" target="_blank">rook
          <svg class="svg">
            <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
          </svg>
        </a> piece moves and attacks horizontally (along rows) or vertically (along columns), through any number of unoccupied squares</p>
    </li>
    <li>
      <p>In chess the <a href="https://en.wikipedia.org/wiki/Queen_(chess)" class="external-link" target="_blank">queen
          <svg class="svg">
            <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
          </svg>
        </a> piece moves and attacks horizontally (along rows), vertically (along columns), or diagonally (along major and minor diagonals), through any number of unoccupied squares</p>
    </li>
  </ul>
  <p><img src="https://user-images.githubusercontent.com/64609529/191106509-ca9b6626-b00c-4e4a-b63f-feaaa9eef633.png" alt="conflict" width="450"></p>

  <h2 id="advanced">Advanced</h2>
  <p>Our advanced content is intended to throw you in over your head, requiring you to solve problems with very little support or oversight, much like you would as a mid or senior level engineer.</p>
  <ul class="task-list">
    <li class="task-list-item">
      <p><input type="checkbox" class="md-task"> Optimize the time and/or space complexity of your solvers. Here are some ideas:</p>
      <ul class="task-list">
        <li class="task-list-item"><input type="checkbox" class="md-task"> Consider the memory usage of your solver:
          <ul>
            <li>Do you have to allocate and duplicate an entire board?</li>
            <li>Can you re-use the board?</li>
            <li>Can you get by with less information?</li>
          </ul>
        </li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> Consider what work you can avoid doing:
          <ul>
            <li>Are you doing any work early in the algorithm that you can tell will be fruitless?</li>
            <li>How much work do you do on paths which are obviously wrong?</li>
          </ul>
        </li>
      </ul>
    </li>
    <li class="task-list-item">
      <p><input type="checkbox" class="md-task"> Use <a href="http://jsperf.com/" class="external-link" target="_blank">JSPerf
          <svg class="svg">
            <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
          </svg>
        </a> or <a href="https://benchmarkjs.com/" class="external-link" target="_blank">BenchmarkJS
          <svg class="svg">
            <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
          </svg>
        </a> to benchmark your code. Use the results to improve your code. Notate changes in your commit messages</p>
    </li>
    <li class="task-list-item">
      <p><input type="checkbox" class="md-task"> What symmetries in the chess board can you exploit to optimize your solution? Do it!</p>
    </li>
    <li class="task-list-item">
      <p><input type="checkbox" class="md-task"> Implement a solution using bitwise operators</p>
      <ul class="task-list">
        <li class="task-list-item"><input type="checkbox" class="md-task"> Read some of these additonal resources about bitwise operations:
          <ul>
            <li><a href="http://en.wikipedia.org/wiki/Bitwise_operation" class="external-link" target="_blank">Wikipedia on bitwise operations
                <svg class="svg">
                  <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
                </svg>
              </a></li>
            <li><a href="http://www.cprogramming.com/tutorial/bitwise_operators.html" class="external-link" target="_blank">C Programming tutorial on bitwise operators
                <svg class="svg">
                  <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
                </svg>
              </a>
              <ul>
                <li>This tutorial is in C, another programming language where bitwise operators are more common, but is also applicable to JavaScript.</li>
              </ul>
            </li>
            <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators" class="external-link" target="_blank">MDN on bitwise operators
                <svg class="svg">
                  <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
                </svg>
              </a></li>
          </ul>
        </li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> Try devising your own bitshifting solution. How will you interact with the problem in bits?</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> Implement <a href="http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.51.7113&amp;rep=rep1&amp;type=pdf">Martin Richards's bitwise n-queens solution algorithm</a>, in JavaScript</li>
      </ul>
    </li>
  </ul>
  <p><em>Optional</em></p>
  <ul class="task-list">
    <li class="task-list-item"><input type="checkbox" class="md-task"> Play with Hack Reactor's own Ruan Pethiyagoda's <a href="https://twitter.com/ruanpethiyagoda/status/332992908565295104" class="external-link" target="_blank">n-queens solution tweet
        <svg class="svg">
          <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
        </svg>
      </a> by either:
      <ul class="task-list">
        <li class="task-list-item"><input type="checkbox" class="md-task"> Writing a blog post that deciphers the tweet for a lay-programmer</li>
        <li class="task-list-item"><input type="checkbox" class="md-task"> Trying to improve on the speed of his algorithm without exceeding the character limit for a tweet</li>
      </ul>
    </li>
  </ul>
  <h2 id="nightmare-mode">Nightmare Mode</h2>
  <ul class="task-list">
    <li class="task-list-item"><input type="checkbox" class="md-task"> <a href="https://en.wikipedia.org/wiki/Parallel_computing" class="external-link" target="_blank">Parallelize
        <svg class="svg">
          <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
        </svg>
      </a> your solution then implement it using <a href="https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers" class="external-link" target="_blank">HTML5 web workers
        <svg class="svg">
          <use href="/assets/images/svg/svg-sprite-action-symbol.svg#ic_launch_24px"></use>
        </svg>
      </a></li>
  </ul>
</div>
