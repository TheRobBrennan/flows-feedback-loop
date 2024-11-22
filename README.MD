# Project Setup

This project requires certain dependencies to be installed for proper functioning. Follow the instructions below to set up your environment.

## Conda Environment

To create a conda environment with Python 3.12, use the following command:

```sh
conda create -y --name crewai-flows-feedback-loop python=3.12 
conda activate crewai-flows-feedback-loop
pip install -r requirements.txt
```

To deactivate an active environment, use

```sh
conda deactivate
```

## Create Flow with Crews

1. **Create a New Flow:**
   - Run the following command to create a new flow named `self_evaluation_loop_flow`:

     ```bash
     crewai create flow self_evaluation_loop_flow
     ```

   - Navigate into the newly created directory:

     ```bash
     cd self_evaluation_loop_flow
     ```

2. **Install Dependencies:**
   - Run the following command to install all necessary dependencies:

     ```bash
     crewai install
     ```

3. **Activate the Environment:**
   - **Mac:**

     ```bash
     source .venv/bin/activate
     ```

   - **Windows:**

     ```bash
     .venv\Scripts\activate
     ```

4. **Set Python Instance for IDE:**
   - **Mac:**

     ```bash
     which python
     ```

   - **Windows:**

     ```bash
     where python
     ```

   - Use the output to set the Python instance in your IDE.

5. **Add Crews to the Flow:**
   - Create a crew named `shakespeare_crew` to generate X posts:

     ```bash
     crewai flow add-crew shakespeare_crew
     ```

   - Create a crew named `x_post_review_crew` to review the posts created by `shakespeare_crew`:

     ```bash
     crewai flow add-crew x_post_review_crew
     ```
