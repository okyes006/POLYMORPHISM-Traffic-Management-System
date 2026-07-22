# POLYMORPHISM–Traffic-Management-System

## Introduction

This repository contains a Python solution for the **Smart Traffic Management System** case study, an exercise in object-oriented programming focused on **polymorphism**.

A smart city relies on several kinds of intelligent traffic devices — traffic lights, speed cameras, pedestrian signals, and (eventually) emergency sirens. Every device receives the same command, `activate()`, but each one is expected to carry out a different task depending on what kind of device it is. Polymorphism makes this possible: code that calls `activate()` doesn't need to know or check which specific device it's talking to.

## What the code does

- Defines a parent class, `TrafficDevice`, with a generic `activate()` method.
- Defines three child classes — `TrafficLight`, `SpeedCamera`, and `PedestrianSignal` — each overriding `activate()` with its own behaviour.
- Creates one object of each class, stores them together in a single list, and activates all of them in a loop **without checking their types**.
- Adds a fourth child class, `EmergencySiren`, to show that new device types can be introduced later **without modifying the existing activation loop** — the loop already works for any `TrafficDevice` subclass.

## File

- `traffic_system.py` — full solution with all classes and a `main()` function demonstrating the activation loop.

## Running it

```bash
python3 traffic_system.py
```

Expected output:

```
[TL1] Traffic light cycling: RED -> YELLOW -> GREEN.
[SC1] Speed camera scanning passing vehicles for speed violations.
[PS1] Pedestrian signal showing WALK sign.
[ES1] Emergency siren blaring — clearing the intersection!
```
