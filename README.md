# RunTurnStopBar
Run Turn Stop module for Motorcycle or third stop light for cars / trucks.
Not satisfied with the current offerings of RTS module add ons for motorcycle, this project is my view of what a RTS block for Motorcycles (or third brake light for cars & trucks) should be.

/*
 * Tailight RTS bar
 * animated Run, Turn, Stop leds for motorcycle
 * 
 * Modes:
 * RUN; Cylon or Night Rider style bouncing light
 * LTURN; led block repeatedly chasing to the Left
 * RTURN; led block repeatedly chasing to the Right
 * HAZ; unknown 
 * STOP; same as current mode, with LED bar inversed
 *        possibly including {triple flash + max Intensity} for STOPmode.
 *
 *
 *   O     O    L3,R3
 *    O   O     L2,R2
 *     O O      L1,R1
 *
 *
 *  Status Register
 *  xxxFIBLR  /Flash/Inverse/Stop/Left/Right
 *
 *   Possible light modes:
 *    xx00 (0) run
 *    xx01 (1) right turn
 *    xx10 (2) left turn
 *    xx11 (3) hazard
 *    x1xx     Brake+
 *    1xxx     Inverse+
 *   1xxxx     Flash+   // Clock bit for Flash
 *   
 */
