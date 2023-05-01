# Lab 10: Blockchain
## From Prof. Lu's GitHub Repo:
### Instructions
1. Study the GitHub [repository](https://github.com/kevinwlu/iot) Lesson 10
2. Run hash_value.py twice and compare results
   ```sh
   $ cd ~/iot/lesson10
   $ cat hash_value.py
   $ py -3.9 hash_value.py
   $ py -3.9 hash_value.py
   ```
3. Run snakecoin.py
   From the same directory:
   ```sh
   $ cat snakecoin.py
   $ py -3.9 snakecoin.py
   ```
4. Run snakecoin-server-full-code.py on Terminal 1 and mine a new block on Terminal 2
   From the same directory:
   - Terminal 1: Run the SnakeCoin server at http://127.0.0.1:5000/
   ```sh
   $ cat snakecoin-server-full-code.py
   $ py -3.9 snakecoin-server-full-code.py
   ```
   - Terminal 2: Create a transaction and mine a new block at http://127.0.0.1:5000/mine
   ```sh
   $ Invoke-RestMethod "http://localhost:5000/txion" -ContentType 'application/json' -Method Post -Body '{"from": "akjflw", "to":"fjlakdj", "amount": 3}'
   $ Invoke-RestMethod "http://localhost:5000/mine"
   ```
5. Clone Python blockchain app and uncomment the last line of node_server.py
   - Uncomment the last line of node_server.py (remove the `#` at the beginning of the line)
   ```sh
   $ git clone https://github.com/satwikkansal/python_blockchain_app.git
   $ cd ~/python_blockchain_app
   $ nano node_server.py
   ```
6. Run node_server.py on Terminal 1 and run_app.py on Terminal 2
   - Terminal 1: Run node_server.py (Press Ctrl+C to quit)
   ```sh
   $ py -3.9 node_server.py
   ```
   - Terminal 2: Run run_app.py (Press Ctrl+C to quit)
   ```sh
   $ cd ~/python_blockchain_app
   $ py -3.9 run_app.py
   ```
   - Go to YourNet running at http://127.0.0.1:5000/
   - Enter `Block #1` into the box, enter your name where indicated, click "Post" and then "Request to mine"
   - Navigate to http://127.0.0.1:8000/mine to see "Block #1 is mined"
   - At YourNet, click "Resync" to view Block #1
### [Lesson 10: Blockchain](lesson10/README.md)
