
class Person{
					constructor(name, age, address, interests){
						this.name = name;
						this.age = age;
						this.address = address;
						this.interests = interests;
					};
					greeting(){
						console.log(`Hi! I'm ${this.name}.`)
					};
					farewell(){
						console.log(`Hi! I'm ${this.name}. Now, ${this.name} has left the building. Bye for now!!!`)
					}
				}

				var person1 = new Person('Dilip', 25, 'Merihaka', 'travelling');
				person1.greeting();
				person1.farewell();

				// To create the subclass which is based on the prevous class (here class Person), we use the extends keyword as:
				class Teacher extends Person {
					constructor(name, age, address, interests, subject, grade){
						super(name, age, address, interests);
						this.subject = subject;
						this.grade = grade;
					}
					get subject(){
						return this._subject;
					}
					set subject(newSubject){
						this._subject = newSubject;
					}

				}
