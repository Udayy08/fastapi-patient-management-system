# FastAPI Patient Management System

A simple, fully functional RESTful API built with FastAPI and Pydantic to manage patient records. It uses a local JSON file (`patients_api_format.json`) as a mock database.

## Features

- **CRUD Operations**: Create, Read, Update, and Delete patient records.
- **Data Validation**: Uses Pydantic models for request validation.
- **Computed Fields**: Automatically calculates a patient's BMI and health verdict (Underweight, Normal, Overweight, Obese) based on height and weight.
- **Sorting**: Sort patients by height, weight, or BMI in ascending or descending order.

## Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/` | Root endpoint, returns a welcome message. |
| `GET` | `/about` | About endpoint. |
| `GET` | `/view` | Retrieve all patient records. |
| `GET` | `/patient/{patient_id}` | Retrieve a specific patient by ID. |
| `GET` | `/sort` | Sort patients based on `height`, `weight`, or `bmi`. Use `order=asc` or `order=desc`. |
| `POST` | `/create` | Create a new patient record. |
| `PUT` | `/edit/{patient_id}` | Update an existing patient record. |
| `DELETE`| `/delete/{patient_id}`| Delete a patient record. |

## Setup and Running Locally

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Udayy08/fastapi-patient-management-system.git
   cd fastapi-patient-management-system
   ```

2. **Set up a virtual environment** (recommended):
   ```bash
   python -m venv .venv
   # On Windows use: .venv\Scripts\activate
   # On Linux/macOS use: source .venv/bin/activate
   ```

3. **Install dependencies**:
   This project uses `uv`/`pyproject.toml`. You can install the dependencies via:
   ```bash
   pip install -e .
   ```

4. **Run the FastAPI server**:
   ```bash
   uvicorn main:app --reload
   ```

5. **API Documentation**:
   Once running, you can access the interactive API documentation at:
   - **Swagger UI**: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
   - **ReDoc**: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

## Technologies Used

- [FastAPI](https://fastapi.tiangolo.com/)
- [Pydantic](https://docs.pydantic.dev/)
- Python 3.13+
