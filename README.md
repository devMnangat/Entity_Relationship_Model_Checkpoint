**Entities:**

1. Gymnasium
    - gym_id (Primary Key)
    - name
    - address
    - phone_number

2. Member
    - member_id (Primary Key)
    - last_name
    - first_name
    - address
    - date_of_birth
    - gender
    - gym_id (Foreign Key referencing Gymnasium)

3. Session
    - session_id (Primary Key)
    - sport_type
    - schedule
    - max_capacity
    - gym_id (Foreign Key referencing Gymnasium)

4. Coach
    - coach_id (Primary Key)
    - last_name
    - first_name
    - age
    - specialty
    - gym_id (Foreign Key referencing Gymnasium)

**Relationships:**

1. Member attends Session (Many-to-Many)
    - member_id (Foreign Key referencing Member)
    - session_id (Foreign Key referencing Session)

2. Session conducted by Coach (Many-to-Many)
    - session_id (Foreign Key referencing Session)
    - coach_id (Foreign Key referencing Coach)
