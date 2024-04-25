Overview: 

The program follows the MVC architectural pattern, which divides it into three main parts: model, view, and controller, each with its own responsibilities. 

ConwayController (controller package) 

This class serves as the controller in the Model-View-Controller (MVC) architectural pattern. It initializes the model (ConwayModel) and view (ConwayView) components. 

Provides methods to start and stop the simulation, compute the next generation of the game, and toggle cell states. 

The main method allows users to input the size of the game board and initiates the controller accordingly. 

ConwayModel (model package) 

Represents the model component responsible for managing the game state. 

Initializes and maintains the game grid, which is a 2D array of boolean values representing the state of each cell. 

Provides methods to compute the next generation of the grid based on Conway's rules and to toggle the state of individual cells. 

ConwayView (view package) 

This class implements the view component responsible for displaying the game interface. 

Extends JFrame to create the main application window. 

Renders the game grid as a JPanel with cells represented by colored squares. 

Provides buttons to start and stop the simulation. 

Implements mouse listeners to allow users to interactively toggle cell states by clicking on the grid. 

 

Design: 

 

Model-View-Controller (MVC) Architecture: 

Model (ConwayModel): Responsible for managing the game state, implementing Conway's Game of Life rules, and maintaining the grid data structure. 

View (ConwayView): Handles the graphical user interface (GUI) aspects, including rendering the game grid and providing user interaction elements like buttons and mouse listeners. 

Controller (ConwayController): Acts as an intermediary between the model and view components, coordinating user input, updating the model state, and refreshing the view. 

Swing GUI for User Interface: 

Java Swing is used to create the graphical user interface (GUI) for the application. 

Swing components such as JFrame, JPanel, and JButton are utilized to build the main window, display the game grid, and provide control buttons, respectively. 

Random Initialization of Game Grid: 

The initial state of the game grid is randomly generated using the Random class from the Java standard library. 

This design choice adds variability to the initial configuration of the game, leading to different patterns and behaviors in each simulation run. 

Separation of Concerns: 

Each class (ConwayModel, ConwayView, ConwayController) is responsible for a specific aspect of the application's functionality, making it easier to understand and modify. 

Simulation Thread: 

The simulation is executed in a separate thread (simulationThread) to prevent blocking the main GUI thread. 

By running the simulation in a background thread, the GUI remains responsive and can handle user input and updates while the simulation is running. 

Dynamic Grid Size: 

Users are prompted to input the size of the game board (N x N) when launching the application. 

This design choice allows users to customize the size of the game grid, accommodating different preferences and scenarios. 

Interactive Cell Toggling: 

Users can interactively toggle the state of individual cells by clicking on them in the game grid. 

This feature enhances user engagement and allows users to experiment with different patterns and configurations in real-time. 

 

 

Features: 

 

Graphical User Interface (GUI): 

The application has a graphical interface built using Swing components. 

It includes a main window (ConwayView) where the game grid is displayed along with control buttons. 

Game Grid Display: 

The game grid is displayed as a grid of cells on the GUI. 

Each cell is represented by a colored square indicating its state (alive or dead). 

Control Buttons: 

"Start" button: Initiates the simulation, allowing the game to progress through generations automatically. 

"Stop" button: Stops the simulation, halting the automatic progression of generations. 

Interactive Cell Toggling: 

Users can interactively toggle the state of individual cells by clicking on them. 

Clicking on a cell changes its state between alive and dead. 

Dynamic Grid Size: 

Users can input the size of the game board (N x N) through a dialog box when the application starts. 

The size of the game grid is dynamically adjusted based on user input. 

Simulation Thread: 

The simulation is executed in a separate thread (simulationThread) to ensure smooth operation of the GUI while the simulation is running. 

The simulation progresses automatically with a delay of 1 second between generations. 

Conway's Game of Life Rules Implementation: 

The program implements the rules of Conway's Game of Life to compute the next generation of the game grid. 

Cells evolve based on the number of neighboring live cells according to the specified rules. 

Random Initialization: 

The initial state of the game grid is randomly generated upon instantiation of the model (ConwayModel). 

Grid Update: 

The GUI updates to reflect changes in the game grid after each generation computation. 

How to Run: 

 

Run the program by executing the main class ‘ConwayController’. 

 

Assumptions: 

 

Random Initialization of Game Grid: 

Assumption: The initial state of the game grid is randomly generated using the Random class. 

Fixed Time Interval for Generation Computation: 

     Assumption: Each generation computation occurs at a fixed time     

     interval of 1 second. 

No Maximum Grid Size Limitation: 

     Assumption: There is no predefined maximum limit on the size of     

     the game grid that users can input. 

Single-threaded GUI Interaction: 

     Assumption: User interaction with the GUI occurs on the main GUI    

     thread. 

No Limitation on Toggle Cell State Interaction: 

     Assumption: Users can toggle the state of any cell in the grid,  

     regardless of its current state or neighboring cells. 

GUI Responsiveness During Simulation: 

     Assumption: The GUI remains responsive and updates in real-time  

     during simulation execution. 

 

Limitations: 

 

Grid Size Constraints: 

While the program allows users to input the size of the game grid dynamically, there might be practical limitations on the maximum grid size based on system resources (e.g., memory). Handling very large grid sizes efficiently could be a challenge and might require optimizations or alternative strategies. 

 
