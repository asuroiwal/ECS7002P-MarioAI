
# MarioGroupE

This is a Java project of Mario Procedural Content Generation using search-based algorithm. This project is based on the Mario AI research project. 

## Running the tests

To run the test, the range and interval of search spaces need to be defined for each paramter in the **LevelGenerator.java** file. 

```
searchSpace.add(newSearchSpace(0.05f, 0.2f, 2e-4f));
```

Then, set values to the parameters of **idealFloorGapCount** and **idealEnemyCount**.

```
int idealFloorGapCount = 70;
int idealEnemyCount = 60;
```

After that, create the class that carries out the search-based method. In the function **setParameters**, give a value of iterations (10000 in this case) to instruct the program to run search for 10000 times.

```
RMHC hillClimber = new RMHC();
generator.setParameters(hillClimber.evolve(generator, 10000));
hillClimber.evaluate(getLevel(null, generator), true);
```

Finally, run the progam and a list of performance results will be displayed

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

* **Tianhua Zhou**
* **Abhishek Suroiwal**

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## Acknowledgments

* The code from the project **ECS7002P-MarioAI** by the research group, GAIGResearch
