# chill-game
The game: rock paper scissors
#include <iostream>
#include <ctime>
using namespace std;
int main() {
	setlocale(LC_ALL, "Russian");
	srand(time(NULL));
	while (true) {
		int player;
		int bot;
		cout << "Хотите сыграть в Камень Ножницы Бумага? 1-Да 2-Нет " << endl;
		cin >> player;
		switch (player) {
		case 1:
			cout << "Выберите 1.Бумага 2.Камень 3.Ножницы " << endl;
			cin >> player;
			bot = rand() % 3 + 1;
			if (bot == 1)
				cout << "Компьютер выбрал: Бумага " << endl;
			else if (bot == 2)
				cout << "Компьютер выбрал: Камень " << endl;
			else if (bot == 3)
				cout << "Компьютер выбрал: Ножницы " << endl;
		if (player == bot) {
			cout << "Ничья!" << endl;
		}
		else if ((player == 1 && bot == 2) ||
			(player == 2 && bot == 3) ||
			(player == 3 && bot == 1)) {
			cout << "Вы победили" << endl;
		}
		else {
			cout << "Вы проиграли" << endl;
		}
		break;
	case 2:
		cout << "Нет? Тогда Удачи!" << endl;
		return 0;
	default: cout << " Я не знаю такого значения!" << endl;
		break;
	    }
	}
	return 0;
}
