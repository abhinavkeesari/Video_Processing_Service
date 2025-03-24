#YouTube Clone - Video Processing Platform

#Tech Stack
TypeScript
Next.js
Express.js
Docker
FFmpeg
Firebase Auth
Firebase Functions
Firebase Firestore
Google Cloud Storage
Google Cloud Pub/Sub
Google Cloud Run

Developing a cloud-based video-sharing platform with secure video uploads, transcoding, and streaming.

Implementing a video processing pipeline using Cloud Storage, Pub/Sub, and Cloud Run to handle raw and processed videos.

Designing a Next.js web client hosted on Cloud Run, integrating Firebase Auth for secure user authentication.

Building an API layer with Firebase Functions to fetch and serve video metadata from Cloud Firestore.

FFmpeg for video transcoding, ensuring optimized playback across multiple devices.

-------------------------------------------------------------------------------------------------------
System Architecture Overview:-

Cloud Storage:
Stores raw (uploaded) and processed (transcoded) videos.

Pub/Sub:
Triggers the video processing service by sending messages when new videos are uploaded.

Video Processing Service (Hosted on Cloud Run, private):
Listens to Pub/Sub messages.
Transcodes videos and uploads results back to Cloud Storage

Cloud Firestore:
Manages video metadata (e.g., title, duration, processing status)

Next.js Web Client (Hosted on Cloud Run, public):
Serves the YouTube-like frontend.
Communicates with Firebase Functions (API backend) to fetch data.

Firebase Functions:
Handle business logic (e.g., authentication, video metadata retrieval).
