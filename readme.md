# Potato Disease Classification
Potato Disease Classification app takes an image of potato leaf and tells whether potato is healthy, early blight or late blight with confidence. It is built using CNN and deep learning techniques.

## Frontend Preview
![ UI](images/f1.png)  

![ UI](images/f2.png)

## Setup for Python:

1. Install Python ([Setup instructions](https://wiki.python.org/moin/BeginnersGuide))

2. It is advisable to create a virtual environment using pip or conda and activate it to prevent dependencies issues
   **Create a virtual environment using Conda**:
   ```sh
   conda create -p venv python==3.9 -y
   ```
   **Activate the virtual environment**:
   ```sh
   conda activate venv/
   ```
3. **Install dependencies**:
   ```sh
   pip install -r requirements.txt
   ```


## Setup for ReactJS

1. Install Nodejs ([Setup instructions](https://nodejs.org/en/download/package-manager/))
2. Install NPM ([Setup instructions](https://www.npmjs.com/get-npm))
3. Install dependencies

```bash
cd frontend
npm install --from-lock-json
npm audit fix
```



4. Change API url in `.env` accordingly.



## Training the Model

1. Download the data from [kaggle](https://www.kaggle.com/arjuntejaswi/plant-village).
2. Only keep folders related to Potatoes.
3. Run Jupyter Notebook in Browser.

```bash
jupyter notebook
```
while using virtual environment, run following command before running notebook.
```
pip install ipykernel
```

4. Open `training/training.ipynb` in Jupyter Notebook or visual studio code.
5. Update the path to dataset.
6. Run all the Cells one by one.
7. Copy the model generated and save it with the version number in the `saved_models` folder.

## Running the API

### Using FastAPI

1. Get inside `api` folder

```bash
cd api
```

2. Run the FastAPI Server using uvicorn

```bash
uvicorn main:app --reload --host 0.0.0.0
```

3. Your API is now running at `0.0.0.0:8000`

You can also use this command in terminal to run api
```
python api/main.py
```
## Running the Frontend

1. Get inside `api` folder

```bash
cd frontend
```

2. In`.env`, update `REACT_APP_API_URL` to API URL if needed.
3. Run the frontend

```bash
npm start
```





