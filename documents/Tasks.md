# Summary
- [Milestones](#milestones)
    - [Island shape generation](#island-shape-generation)
    - [Biome Region Assignment](#biome-region-assignment)
    - [WFC with Biome Constraints](#wfc-with-biome-constraints)
- [Tips](#tips) 

# Milestones

## Island shape generation
Generate a rough island mask just to define it's size/shape. 
Use perlin noise for more "organic" shapes

## Biome Region Assignment
Fill the island mask with random seeds for biomes (amount of biomes in an island = amount of seeds)
Assign each seed to a biome using Voronoi (so same biomes wont touch each other)

## WFC with Biome Constraints
Go through each biome and fill them using rulesets for each biome (e.g: Tree tile -> Forest, Rock tile -> Desert)
Tiles near the mask edge have higher probability of being edge/border types


# Tips
- Start simple: get a basic circular island with one biome working first
- Edge tiles are crucial - you'll need variants for different biome types (grassy cliff, desert cliff, etc.)
- Consider having "buffer zones" between biomes rather than hard transitions
- You might want some tiles that CAN appear in multiple biomes (rocks, dirt) to help transitions feel natural