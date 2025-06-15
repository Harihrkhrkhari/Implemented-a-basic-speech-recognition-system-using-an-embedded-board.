#include <SoftwareSerial.h>
#include "VoiceRecognitionV3.h"

// Create software serial on pins 2 and 3
SoftwareSerial mySerial(2, 3);

// Create VoiceRecognition object
VR myVR(mySerial);

// Define command codes (index numbers)
#define CMD_LIGHT_ON 0
#define CMD_LIGHT_OFF 1

// Output pin
#define DEVICE 13

uint8_t records[7]; // save record
uint8_t buf[64];    // receive buffer

void setup() {
