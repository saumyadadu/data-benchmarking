# Data-benchmarking


## 📊 Spatial Data Structure Performance Analysis for Restaurant Search

This project analyzes the performance of three spatial data structures—**Linear Search**, **Grid-based Spatial Index**, and **R-tree**—to optimize nearby restaurant search queries in food delivery applications like Swiggy or Zomato. 

### 🔍 Objective

The goal is to:
- Compare the performance of different spatial indexing methods
- Identify the best structure for various dataset sizes
- Understand trade-offs between simplicity, speed, and memory usage

### 🛠️ Methods Implemented

1. **Linear Search (Baseline)**
   - Simple iteration through all restaurants
   - Time Complexity: `O(n)`
   - Best for small datasets

2. **Grid-based Spatial Index**
   - Divide area into fixed-size grids and search intersecting cells
   - Time Complexity: `O(k)` (k = points in nearby cells)
   - Balanced approach for medium-scale data

3. **R-tree Index**
   - Hierarchical tree of bounding rectangles
   - Time Complexity: `O(log n + k)`
   - Best performance and scalability for large datasets

### 🧪 Experimental Setup

- **Dataset**: 10,000 synthetic restaurants within Bangalore
- **Search Radius**: 2 km
- **Queries**: 100 random locations
- **Environment**: Python 3.8, Intel i7, 16GB RAM, Ubuntu 20.04

### ⚡ Results (Avg Query Time)

| Method       | Time (ms) | Improvement |
|--------------|-----------|-------------|
| Linear Search| 15.42     | -           |
| Grid-based   | 3.87      | ~75% faster |
| R-tree       | 2.31      | ~85% faster |

### 💡 Key Recommendations

- **< 1,000 entries**: Use Linear Search
- **1,000–10,000 entries**: Use Grid-based Indexing
- **> 10,000 entries**: Use R-tree for best performance

### 📈 Future Enhancements

- Parallel search for Linear method
- Dynamic grid size tuning
- Bulk R-tree loading optimization
- Filter support (e.g., rating, cuisine)
- Real-time updates and caching

### 📚 References

- Guttman, A. (1984). *R-trees: A Dynamic Index Structure for Spatial Searching*
- Bentley, J.L. (1975). *Multidimensional Binary Search Trees*
- PostgreSQL & MongoDB spatial indexing documentation

