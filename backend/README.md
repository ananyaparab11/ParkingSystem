# ParkOS — Backend

## Files
| File               | Purpose                            |
|--------------------|------------------------------------|
| `main.py`          | FastAPI app with all API routes    |
| `models.py`        | Database table definitions         |
| `schemas.py`       | Request/response data validation   |
| `database.py`      | SQLite database connection         |
| `requirements.txt` | Python dependencies                |

## Setup
```bash
pip install -r requirements.txt
```

## Run
```bash
uvicorn main:app --reload
```
Backend runs at: http://localhost:8000

## Interactive API Docs
Visit http://localhost:8000/docs to test all endpoints in your browser.

## All Endpoints
| Method | URL                        | What it does                     |
|--------|----------------------------|----------------------------------|
| GET    | /slots                     | All floors + slot availability   |
| GET    | /slots?vehicle_type=X      | Filter slots by vehicle type     |
| GET    | /admin/floors              | List all floors                  |
| POST   | /admin/floor               | Add or update a floor            |
| DELETE | /admin/floor/{floor_no}    | Delete a floor                   |
| POST   | /user/park                 | Park a vehicle                   |
| POST   | /user/exit                 | Exit a vehicle                   |
| GET    | /user/search?veh=XX        | Search vehicle by number         |
| GET    | /logs                      | All parking logs                 |
| GET    | /fines                     | All fines                        |
| POST   | /sensor/verify             | Sensor check (fine if wrong slot)|
| GET    | /health                    | Health check                     |

## Database
SQLite file `parking.db` is auto-created in the backend folder on first run.
No setup needed.
