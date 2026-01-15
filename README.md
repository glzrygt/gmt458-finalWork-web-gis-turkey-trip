# Turkey Trip – Full Stack Web GIS Game
👉 https://main.drz4hngnyw4u5.amplifyapp.com
## Project Overview
Turkey Trip is a full-stack Web GIS game developed as the final project for the
GMT 458 – Web GIS course. The application combines interactive mapping,
spatial data, and backend services in a game-based learning environment.

Players are asked to guess Turkish cities using either license plate numbers
or local music clues. The system records user progress and scores using a
NoSQL database.

---

## Implemented Assignment Items

### Managing Different User Types
- The system supports guest users who can directly play the game.
- Usernames are stored and tracked for score history and leaderboard purposes.
- Different permissions are implicitly defined (player vs system-controlled data).

---

### CRUD Operations on Spatial Data
Spatial city data is handled through full CRUD logic:
- **Create:** Correctly guessed cities are saved as visited locations.
- **Read:** City and province data is retrieved from the backend API.
- **Update:** User progress and scores are updated during gameplay.
- **Delete:** Game sessions and temporary data are reset when restarting the game.

Filtering and interaction are performed through the map interface.

---

### NoSQL Database Usage
- MongoDB is used as the main database system.
- Collections include users, cities, visits, and scores.
- The schema-less structure allows flexible handling of heterogeneous game data.

---

### API Development
The backend API exposes both spatial and non-spatial resources.

**Spatial endpoints:**
- `GET /api/cities` – returns city data with geographic coordinates
- `POST /api/visits` – creates a new visited spatial feature

**Non-spatial endpoints:**
- `POST /api/score` – saves user scores
- `GET /api/leaderboard` – returns leaderboard information

All endpoints were tested using Postman.

---

### Authentication
- A lightweight authentication mechanism is implemented using username-based login.
- User identity is persisted using localStorage and backend records.
- This approach was selected to keep the game accessible and fast.

---

### Performance Monitoring
- MongoDB indexes were applied to frequently queried fields such as city name
  and license plate number.
- Query behavior with and without indexing was observed and compared.

---

### Performance Testing
- Load testing was conceptually designed using Artillery.
- The system was tested under multiple concurrent requests to observe
  response time behavior.
- Results were evaluated to identify potential bottlenecks.

---

## Technologies Used
- **Frontend:** HTML, CSS, JavaScript, Leaflet, D3.js
- **Backend:** Node.js, Express
- **Database:** MongoDB (NoSQL)
- **Deployment:** AWS Amplify (Frontend), MongoDB Atlas

---

## Project Purpose
This project demonstrates how Web GIS concepts such as spatial data handling,
API-based architectures, and NoSQL databases can be integrated into an
interactive full-stack application.

---

## Course Information
GMT 458 – Internet Based Geographical Information Systems  
Final Assignment – Full Stack Web GIS
