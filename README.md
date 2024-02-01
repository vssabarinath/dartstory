# dartstory
import 'dart:io';

void main() {
  print('Welcome to the Biodata Generator!');
  print('Please provide the following information:');

  // Collecting user information
  print('Name: ');
  String name = stdin.readLineSync() ?? '';

  print('Phone number: ');
  String phoneNumber = stdin.readLineSync() ?? '';

  print('Age: ');
  int age = int.tryParse(stdin.readLineSync() ?? '') ?? 0;

  print('Height (in cm): ');
  double height = double.tryParse(stdin.readLineSync() ?? '') ?? 0.0;

  print('Weight (in kg): ');
  double weight = double.tryParse(stdin.readLineSync() ?? '') ?? 0.0;

  print('Address: ');
  String address = stdin.readLineSync() ?? '';

  print('Hobbies (comma-separated): ');
  List<String> hobbies = (stdin.readLineSync() ?? '').split(',');

  // Generate and display biodata
  print('\n\nGenerating Biodata...\n');
  print('---------------------------------------');
  print('Name: $name');
  print('Phone Number: $phoneNumber');
  print('Age: $age');
  print('Height: $height cm');
  print('Weight: $weight kg');
  print('Address: $address');
  print('Hobbies:');
  for (String hobby in hobbies) {
    print('- $hobby');
  }
  print('---------------------------------------');
}
