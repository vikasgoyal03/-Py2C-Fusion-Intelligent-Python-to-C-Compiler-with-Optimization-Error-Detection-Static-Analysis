# -Py2C-Fusion-Intelligent-Python-to-C-Compiler-with-Optimization-Error-Detection-Static-Analysis
Py2C Fusion is a Python-based desktop application designed to analyze Python code, detect errors, and translate it into  optimized C code. Built using the tkinter GUI framework, the tool provides an interactive interface for users to input or  load Python scripts, run various analyses, and view results in a structured, readable format. 
The main goal of this project is to simplify the process of identifying code issues and enable high-performance code 
transformation. The application performs multiple automated checks: syntax validation using the ast module, 
unreachable code detection by scanning return paths in functions, and static analysis to identify unsafe practices like 
eval, exec, or use of sensitive modules like os.  
Once validated, the Python code is translated line-by-line into basic C syntax, supporting constructs like variable 
assignments, function definitions, and print statements. This translated code is further passed through a basic C optimizer 
to enhance structure and efficiency.  
Additional features include theme toggling (dark/light mode), output saving, and file loading, making it user-friendly for 
both students and developers. By combining code safety, translation, and optimization, Py2C Fusion offers a practical tool 
for learning and deploying efficient code. 
Py2C Fusion follows a modular and event-driven architecture using Python’s tkinter library to build a 
responsive graphical user interface (GUI). The system is divided into separate functional modules: 
syntax_checker.py, static_anaylzer.py, unreachable_code.py, python_to_c.py, and c_optimizer.py. 
Each module is responsible for a specific analysis or transformation task, promoting maintainability 
and scalability.  
When a user inputs or loads Python code and clicks "Run Analysis", the GUI triggers the 
run_analysis() function. This function sequentially calls:  
• check_syntax() to validate syntax using Python’s ast module.  
• detect_unreachable_code() using a custom AST visitor to identify code after return 
statements.  
• static_analysis() to flag insecure patterns like eval, exec, or import os.  
• translate_python_to_c() to convert basic Python constructs into equivalent C code.  
 optimize_c_code() to refine the generated C output.  
The application uses ScrolledText widgets for input and output areas and supports light/dark themes 
via a global toggle. Communication between modules is done via direct function calls—no external 
APIs or network communication is required. Files can be loaded or saved using filedialog. 
