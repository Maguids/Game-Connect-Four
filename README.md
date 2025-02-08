# Game - Connect Four

This project was developed for the "Artificial Intelligence" course and aims to **develop the game ConnectFour**. The project should include an **A\* algorithm** and a **MCTS algorithm**, although we also included **Minimax with different heuristics and with or without alpha-beta pruning**.

---
<br>

## Programming Language:

<div style = "display: inline_block"><br/>
  <img align="center" alt="python" src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
</div><br/>

<br>

## About the Project:

### Connect Four:
Connect Four is a two-player strategy game. It is played using 42 tokens (21 for each player), and a vertical grid that is 7 columns wide. Each column can hold a maximum of 6 tokens. The two players take turns. A move consists of a player dropping one of his/her tokens into the column of his/her choice. When a token is dropped into a column, it falls until it hits the bottom or the top token in that column. A player wins by creating an arrangement in which at least four of his/her tokens are aligned in a row, column or diagonal.

In this project we **devoleped the game using python** in jupyter notebook in the section <i>"Implementação do Jogo"</i>. Its interface is very simple consisting on a simple print of the matrix as shown below:

<br>

<p align="center">
  <img width="460" height="300" src="https://github.com/user-attachments/assets/ac54c2ef-523a-4c62-b197-e47d8204e26a">
</p>

The game has a Menu that allows the player to decide on the game mode, which can be:
- Player VS Player;
- Player VS Algorithm;
- Algorithm VS Algorithm.

### Algorithms:
- **A\* (A Star)**;
- **Monte Carlo Tree Search**;
- **Minimax** - with and withough pruning.

For **A\*** it was predefined that **only Heuristic 1 can be used**.
However in **Minimax** it is now possible to **choose the Heuristic** and **whether we are using pruning or not**, and it is also possible to **determine the depth that Minimax can reach**. 
In **MCTS**, it is possible to choose **whether it will work based on time or iterations**, and it is possible to define the **time limit** and the **number of iterations**. Regardless of the game mode chosen for MCTS, it is possible to **choose the number of child nodes** that can be selected, that is, each node only has the number of child nodes that it is allowed.

<br>

### Heuristics:

- **Heuristc 1:** Evaluates all sets of four pieces that can be formed that contain the piece that has just been placed, following the following rules for awarding points:
	- A win for player X has a value of +512.
	- A win for player O has a value of -512.
	- A tie has a value of 0.
	- For the intermediate positions, we consider all possible combinations of four aligned pieces (horizontal, vertical or diagonal) and assign the following values:
		- -50 for three pieces of O without X.
		- -10 for two pieces of O without X.
		- -1 for a piece of O without X.
		- 0 for no pieces or a mix of X and O pieces.
		- 1 for an X piece without an O.
		- 10 for two pieces of X without O.
		- 50 for three pieces of X without O.
	- Additionally, a bonus is added depending on who makes the move:
		- +16 to X.
		- -16 to O.

- **Heuristic 2:** This heuristic follows the principle of the previous heuristic, but focuses on analyzing <i>all possible 4-piece segments of the entire board</i>. In an attempt to improve the efficiency and decision-making capacity of algorithms, especially minimax.

- **Heuristic 3:** It's a combination of the board reading from heuristic 2 with the scoring system from heuristic 1.

<br>

## About the repository:

- IA_2324_Trab1.pdf ➡️ Is the statement of the project;
- report_PL3_6_final.ipynb ➡️ Is the work developed in detail and all its code;

<br>

## Link to the course: 

This course is part of the **<u>second semester</u>** of the **<u>second year</u>** of the **<u>Bachelor's Degree in Artificial Intelligence and Data Science</u>** at **<u>FCUP</u>** and **<u>FEUP</u>** in the academic year 2023/2024. You can find more information about this course at the following link:

<div style="display: flex; flex-direction: column; align-items: center; gap: 10px;">
  <a href="https://sigarra.up.pt/fcup/pt/UCURR_GERAL.FICHA_UC_VIEW?pv_ocorrencia_id=529859">
    <img alt="Link to Course" src="https://img.shields.io/badge/Link_to_Course-0077B5?style=for-the-badge&logo=logoColor=white" />
  </a>

  <div style="display: flex; gap: 10px; justify-content: center;">
    <a href="https://sigarra.up.pt/fcup/pt/web_page.inicial">
      <img alt="FCUP" src="https://img.shields.io/badge/FCUP-808080?style=for-the-badge&logo=logoColor=grey" />
    </a>
    <a href="https://sigarra.up.pt/feup/pt/web_page.inicial">
      <img alt="FEUP" src="https://img.shields.io/badge/FEUP-808080?style=for-the-badge&logo=logoColor=grey" />
    </a>
  </div>
</div>
