# Course Allocation Optimization

This repository contains the code and documentation for the final project of the Optimization & Simulation course, focused on optimizing course allocation to faculty members at the ABC School of Business while maximizing their happiness based on preferences. The project also includes a simulation component to handle uncertainty in the number of student groups per course.

## Project Overview

The goal of this project is to:
1. **Optimize** the allocation of courses to faculty members across three trimesters, ensuring compliance with workload constraints (6 credits max per trimester, 10–16 credits annually) and maximizing faculty happiness based on their preference ratings (0–5 scale, where 0 indicates inability to teach).
2. **Simulate** scenarios to account for uncertainty in the number of student groups per course, as the actual number of groups may vary between a minimum and maximum value.

The project uses a linear programming approach implemented with the PuLP library in Python, along with simulation techniques to evaluate different group allocation scenarios.

## Repository Structure

- `opt_sim_v3.ipynb`: Jupyter Notebook containing the main code for the optimization and simulation models, including data preprocessing, model formulation, and results visualization.
- `case_abc.xlsx`: Excel file hosted in the repository containing the dataset with course details (credits, trimester, min/max groups) and faculty preferences.
- `README.md`: This file, providing an overview of the project and instructions for use.

## Dependencies

To run the notebook, you need the following Python libraries:
- pandas
- numpy
- pulp
- matplotlib
- seaborn

Install them using:
```bash
pip install pandas numpy pulp matplotlib seaborn
```

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/Rohaid-Bhatti/CourseAllocationOptimization.git
   ```
2. Open the `opt_sim_v3.ipynb` notebook in Jupyter or Google Colab.
3. Ensure the `case_abc.xlsx` file is accessible (it is hosted in this repository and loaded directly via a raw GitHub link in the notebook).
4. Run the notebook cells sequentially to:
   - Load and preprocess the data.
   - Solve the optimization problem using PuLP.
   - Run simulations to evaluate different group allocation scenarios.
   - Visualize results.

## Data

The dataset (`case_abc.xlsx`) includes:
- **Course Information**: Course code, name, credits, trimester, minimum and maximum number of groups.
- **Faculty Preferences**: Preference ratings (0–5) for each faculty member for each course.

The data is stored in an Excel file and accessed via a URL in the notebook for convenience.

## Assumptions and Limitations

- The simulation assumes a decreasing probability distribution for the number of groups between the minimum and maximum values, as no specific probability distribution was provided.
- The model does not account for the number of students per group or minimum/maximum students per group, which could affect group creation decisions.
- Lack of historical data limits the accuracy of group number predictions.

## Future Improvements

- Collect historical data on student enrollment to improve group number predictions using predictive analytics.
- Incorporate additional constraints, such as maximum students per group or course popularity by trimester.
- Enhance the simulation with more sophisticated probability distributions based on real-world data.

## Contributors

- [r41ss4](https://github.com/r41ss4) (Primary author and copyright owner)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
