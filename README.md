# React_Notes

### Description: Notes about React

## useEffect

useEffect(() => {
  performSideEffect();
}, []);

*   Giving it an empty array acts like componentDidMount as in, it only runs once.

*   Giving it no second argument acts as both componentDidMount and componentDidUpdate, as in it runs first on mount and then on every re-render.

*   Giving it an array as second argument with any value inside, eg , [variable1] will only execute the code inside your useEffect hook ONCE on mount, as well as whenever that particular variable (variable1) changes.

*   If you return a clean up function from your useEffect

useEffect(() => {
  performSideEffect();
  return cleanUpFunction;
}, []);

It will run before every useEffect code run, to clean up for the previous useEffect run. (Except the very first useEffect run)
