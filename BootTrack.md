# BootTrack: A Starknet-Powered Bootcamp Tracker

## 📚 Overview

**BootTrack** is a blockchain-based bootcamp tracker built with Cairo for the Starknet ecosystem. It provides a decentralized and transparent way to manage attendance, assignments, and graduation status for bootcamp participants.

## 🧠 Motivation

This project was inspired by a real experience during the just concluded Starknet blockchain Bootcamp IV. Each week, Serah; who basically handled the attendance and updating the assignment spreadsheet had to remind people (sometimes repeatedly on Zoom) to use their real names so she could mark them properly as present for that particular session. It's quite obvious that the whole process can be very tedious and prone to errors. That got me thinking: what if this could be automated and stored on-chain so future bootcamps don't have to deal with all that manual stress?

BootTrack eliminates the overhead of manual record-keeping by allowing bootcamp organizers to manage participant activity on-chain. It ensures fairness and clarity in graduation criteria and makes the bootcamp more engaging by allowing attendees to track their performance.

Currently, the contract allows anyone to create and retrieve a bootcamp, which ideally should be restricted to verified organizers. That access control isn't in place yet due to time constraints. But it’s something I plan to lock down in future iterations.

## Features

### 👥 Attendee Management

- Organizer can create a bootcamp with session and assignment structure.
- Attendees are registered using their wallet addresses.

### 🧑‍🏫 Tutor Management

- Organizers can add tutors who are allowed to grade assignments.

### 🕒 Attendance System

- Organizers open and close attendance for specific sessions.
- Attendees can mark their attendance only within the open timeframe.
- System prevents double attendance marking.

### 📝 Assignment Grading

- Assignments can be graded by tutors or organizers.
- Supports both single and batch grading per week.

### 🎓 Graduation Evaluation

Graduation is automatically processed based on:

- **Attendance %** (total sessions attended / total sessions)
- **Assignment Score %** (total score / max possible)

Status categories:

- `0` - Not Qualified (<25% attendance)
- `1` - Attendee (≥25%)
- `2` - Graduate (≥50% attendance and ≥50% score)
- `3` - Graduate with Distinction (≥50% attendance and ≥80% score)

### 📊 Data Retrieval

- Get attendee stats (attendance count, assignment score, status)
- Get all attendees in a bootcamp
- Retrieve bootcamp metadata

## 🧱 Data Model

### Structs

- `Bootcamp`
- `AttendeeRecord`
- `AttendanceSession`
- `AssignmentGrade`

### Storage Maps

- `bootcamps`: bootcamp_id → Bootcamp
- `attendee_records`: (bootcamp_id, address) → AttendeeRecord
- `assignment_grades`: (bootcamp_id, week, address) → AssignmentGrade
- `attendance_sessions`: (bootcamp_id, week, session_id) → AttendanceSession
- `individual_attendance`: (bootcamp_id, week, session_id, address) → bool
- `bootcamp_attendee_by_index`: (bootcamp_id, index) → address

## 🧪 Example Usage

1. `create_bootcamp(...)`
2. `register_attendees(...)` (batch mode)
3. `add_tutor(...) add_multiple_tutors(...)`
4. `open_attendance(...)`
5. `mark_attendance(...)`
6. `close_attendance(...)`
7. `grade_assignment(...)` or `batch_grade_assignments(...)`
8. `process_graduation(...)` or `process_all_graduations(...)`

## 🚀 Future Improvements

- NFT Certificate generation for graduates
- ZK-based attendance verification
- Access-based Bootcamp creation and retrieval

## ⚙️ Getting Started

### 🧾 Prerequisites

Make sure you have the following installed globally:

- [Scarb](https://docs.swmansion.com/scarb/) – Cairo package manager
- [Snfoundry](https://github.com/foundry-rs/starknet-foundry) – for testing and interaction
- Node.js (v20 or later)
- Yarn or npm

---

### 📦 Bootstrapping the Contract

1. clone the repository:

2. Run tests (optional):

```bash
scarb test
```

3. Deploy to Starknet (testnet)
   You can use `sncast`, `starkli`, or deploy through a frontend script using `Starknet-Kit`. Be sure to configure your environment and wallet accordingly.

### 🖥️ Running the Frontend

1. Clone the repository
2. Install dependencies:

```bash
yarn install
# or
npm install
```

3. Create a `.env.local` file and configure your environment variables (e.g., contract address, RPC URL, etc.)

```bash
cp .env.example .env.local
```

4. Start the development server:

```
yarn dev
```

### Project Link

[https://boot-track-frontend.vercel.app](https://boot-track-frontend.vercel.app)

### Project Codebase

Frontend Repo
[https://github.com/hmdNetizen/boot-track-frontend](https://github.com/hmdNetizen/boot-track-frontend)

Smart Contract Repo
[https://github.com/hmdNetizen/boot-track-contract](https://github.com/hmdNetizen/boot-track-contract)

### Project Video

https://drive.google.com/file/d/1iVSxT25IOW-D8gJGfTSNGllZK4_fXw8I/view?usp=sharing

### 👤 Author

**Hamed Jimoh**
