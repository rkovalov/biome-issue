# Biome issue demo

This repository demonstrates an issue with Biome (https://github.com/biomejs/biome) where it doesn't extend nested config.

## The issue

When Biome is configured to extend a nested config file, it doesn't work as expected.

## Steps to reproduce

1. Clone this repository
2. Run `npm install`
3. Run `npm run format:lint`

## Expected behavior

Biome should be able to extend the nested config file and ignore tsconfig files.

## Actual behavior

Biome doesnt extend the nested config file and run default config.

## Configuration

The configuration is as follows:

- `biome.json` extends `biome-config/app.json`
- `biome-config/app.json` extends `biome-config/base.json`
