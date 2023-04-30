# Lab 8: Data Analysis
## From Prof. Lu's GitHub Repo:
### Instructions
1. Study the GitHub [repository](https://github.com/kevinwlu/iot) Lesson 8
2. Install Python packages
   ```sh
   $ python -m pip install numpy scipy scikit-learn matplotlib pandas tensorflow keras
   ```
3. Save the Lab 7 Google sheet in CSV format to ~/demo
4. Copy ~/iot/lesson8/plt_final.py and plt_cv2.py to ~/demo
   ```sh
   $ cd ~\demo
   $ cp ~\iot\lesson8\plt_final.py .
   $ cp ~\iot\lesson8\plt_cv2.py .
   ```
5. Edit plt_final.py and plt_cv2.py to read the CSV file with customized plot titles
   ```sh
   $ nano plt_final.py
   ```
   - Set `data` to `read_csv('cpudata.csv')`
   ```sh
   $ nano plt_cv2.py
   ```
   - Set `X` to `read_csv('cpudata.csv', usecols=[1])`
   - Set `y` to `read_csv('cpudata.csv', usecols=[2])`
6. Run plt_final.py and plt_cv2.py
   ```sh
   $ py -3.9 plt_final.py
   $ py -3.9 plt_cv2.py
   ```
### [Lesson 8: Data Analysis](lesson8/README.md)
