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
   $ cd
   ```
   - Terminal 2: Create a transaction and mine a new block at http://127.0.0.1:5000/mine
   ```sh
   $ curl "localhost:5000/txion" -H "Content-Type: application/json" -d '{"from": "akjflw", "to":"fjlakdj", "amount": 3}'
   $ curl localhost:5000/mine
   ```
5. Clone Python blockchain app and uncomment the last line of node_server.py
   - Terminal 1: Uncomment the last line of node_server.py (or search for port=8000) and run (Press Ctrl+C to quit)
   ```sh
   $ git clone https://github.com/satwikkansal/python_blockchain_app.git
   $ cd ~/python_blockchain_app
   $ nano node_server.py
   $ py -3.9 node_server.py
   ```
   - Terminal 2: Run run_app.py (Press Ctrl+C to quit)
   ```sh
   $ vncserver
   $ cd ~/python_blockchain_app
   $ python3 run_app.py
   ```
6. Run node_server.py on Terminal 1 and run_app.py on Terminal 2
   ```sh
   ```
### [Lesson 10: Blockchain](lesson10/README.md)
