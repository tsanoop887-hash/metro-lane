# metro-lane
Intelligent Metro Lane-Selection System Using CNN, GNN, DSA, DQN & Backpropagation
Deep Learning + Graph Learning + Reinforcement Learning Pipeline
📌 Project Overview

This project builds a fully autonomous metro route optimization system that analyzes a metro map image, extracts station structures, builds a graph, learns metro network relationships, and predicts the best lane/route to reach the destination.

It combines:

Image Understanding (CNN – AlexNet/VGG16/ResNet)

Graph Modeling (DSA + Dijkstra)

Graph Neural Networks (GNN – GCN/GAT)

Reinforcement Learning (Deep Q-Network)

Backpropagation across all learning modules

The final agent can:

Detect stations & tracks from a real metro map image

Build a weighted graph

Learn station embeddings

Predict the best path from Start → Destination

Choose lanes correctly at interchanges

Draw the optimal route on the map image

🏗 System Architecture

Below is the full architecture diagram (ASCII for README).

┌──────────────────────────────┐
│         Metro Map Image      │
└───────────────┬──────────────┘
                │
        (1) CNN Feature Extractor
                │
                ▼
     Stations + Track Segments Detected
                │
        (2) Graph Builder (DSA)
                │
                ▼
    Weighted Graph (Nodes + Edges + Distances)
                │
          (3) GNN (GCN/GAT)
                │
                ▼
         Node Embeddings Learned
                │
        (4) DQN Reinforcement Agent
                │
                ▼
       Optimal Lane/Route Prediction
                │
                ▼
     Visualization on Metro Map (Output)


Learning modules (CNN, GNN, DQN) all use BACKPROPAGATION.

⚙️ Key Features
✅ Automatic station detection from image
✅ Graph creation using Dijkstra/BFS
✅ GNN-based structural understanding
✅ DQN agent learns best lane decisions
✅ Final route drawn on the map image
✅ Real-time station-to-station recommendations
✅ Adaptive reinforcement learning behavior
📊 Technology Stack
Component	Technology
Deep Learning	PyTorch, VGG16 / ResNet
Graph Learning	PyTorch-Geometric (GCN/GAT)
Reinforcement Learning	DQN
Image Processing	OpenCV
Graph Algorithms	NetworkX (Dijkstra, adjacency)
Visualization	Matplotlib
📂 Dataset
Input:

A metro map image (PNG/JPG), e.g.:

Bangalore Namma Metro Map

Delhi Metro Map

Any custom metro layout map

Automatically extracted:

Station coordinates

Track connections

Switching nodes

No manual labels required.

🚀 Model Pipeline
1️⃣ CNN – Station & Track Detection

Uses VGG16 / ResNet

Extracts station circles

Extracts colored lines

Outputs (x,y) coordinates

2️⃣ DSA – Graph Construction

Builds adjacency list

Computes edge weights

Runs Dijkstra for shortest path features

3️⃣ GNN – Structural Learning

Learns topology

Learns station embeddings

Generates graph-aware features

4️⃣ DQN – Lane/Route Selection

Input: GNN embeddings + Dijkstra distances

Output: Best next station/action

Reward-based learning

5️⃣ Route Visualization

Final predicted path drawn on map

Yellow = stations

Red = AI-generated optimal route
