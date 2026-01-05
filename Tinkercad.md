# Simulate Linked list
In this project, we use this specific pattern of operations.\n
**(insert 1,2,3,4 and then delete 2)**
## Use parts
- Arduino Uno, LED*4
## Code
```text
//C++

struct Node{
  int data;
  Node* next;
};

Node* head = NULL;
int step = 0;

void insertNode(int value){
  Node* newNode = new Node;
  newNode->data = value;
  newNode->next = head;
  head = newNode;

  Serial.print("Inserted:");
  Serial.println(value);
  printList();
}

void deleteNode(int value){
  Node* temp = head;
  Node* prev = NULL;

  while(temp != NULL && temp->data != value){
    prev = temp;
    temp = temp->next;
  }

  if(temp == NULL){
    Serial.println("Value not found!");
    return;
  }

  if(prev == NULL){
    head = temp->next;
  }else{
    prev->next = temp->next;
  }
  delete temp;

  Serial.print("Deleted: ");
  Serial.println(value);
  printList();
}

void printList(){
  Node* temp = head;
  Serial.print("List:");
  while(temp != NULL){
    Serial.print(temp->data);
    Serial.print(" -> ");
    temp = temp->next;
  }
  Serial.println("NULL");
}

void updateLEDs(){
  for(int i = 2; i <= 5; i++){
    digitalWrite(i, LOW);
  }

  Node* temp = head;
  int pin = 2;
  while(temp != NULL && pin <= 5){
    digitalWrite(pin, HIGH);
    temp = temp->next;
    pin++;
  }
}

void setup(){
  Serial.begin(9600);
  for (int i = 2; i <= 5; i++) {
    pinMode(i, OUTPUT);
  }
}
// In this project, we use this specific pattern of operations
// (insert 1,2,3,4 and then delete 2).
void loop(){
  updateLEDs();
  delay(2000);
  if(step == 0){
    insertNode(1);
  }else if(step == 1){
    insertNode(2); 
  }else if(step == 2){
    insertNode(3); 
  }else if(step == 3){
    insertNode(4);
  }else if(step == 4){
    deleteNode(2); 
  }

  step++;
}
```
## result log
```text
Inserted: 1
List:1 -> NULL
Inserted: 2
List:2 -> 1 -> NULL
Inserted: 3
List:3 -> 2 -> 1 -> NULL
Inserted: 4
List:4 -> 3 -> 2 -> 1 -> NULL
Deleted: 2
List:4 -> 3 -> 1 -> NULL
```
