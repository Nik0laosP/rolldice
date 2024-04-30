// Function to simulate rolling a six-sided die
function rollDie() {
    return Math.floor(Math.random() * 6) + 1;
}

// Function to simulate rolling two dice and returning the sum
function rollTwoDice() {
    return rollDie() + rollDie();
}

// Simulate rolling two dice multiple times and calculate the probability distribution of the sum
function calculateProbabilityDistribution(numRolls) {
    const distribution = {};

    for (let i = 0; i < numRolls; i++) {
        const sum = rollTwoDice();
        if (distribution[sum]) {
            distribution[sum]++;
        } else {
            distribution[sum] = 1;
        }
    }

    // Calculate probabilities
    for (const key in distribution) {
        distribution[key] = distribution[key] / numRolls;
    }

    return distribution;
}

// Example usage
const numRolls = 1000;
const probabilityDistribution = calculateProbabilityDistribution(numRolls);
console.log("Probability Distribution after", numRolls, "rolls:");
console.log(probabilityDistribution);
