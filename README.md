#include <iostream>
#include <stdlib.h>
#include <time.h>
#include <ctime>
#include <windows.h>

using namespace std;
int main()
{
	setlocale(LC_ALL, "Rus");
	string name;
	string bichBonus[2] = { "номера “Свои”"};
	string bichPriz;
	string midBonus[4] = { "номера “Свои”", "мигалки под стекло","откидные номерные рамки." };
	string midPriz;
	string topBonus[5] = { "номера “Свои” и рамка “управление по управлению всеми управлениями”", "люстра на крышу","шторки на номера.","рация настроенная на милицескую волну.","СГУ" };
	string topPriz;
	/*string arrAvto[] = { "Бэха 520 с шильдиками и обвесом М", "Камни 3.5 в китайском обвесе","Eшка 1.8 с амг шильдиками и обвесом китайским","Kамаро на попель моторе экобуст"};
	string avto;*/

	int age = 0, inAge;
	int lvl=0;
	string inPassword,Password, newPassword;
	int a, c, d;
	


	int popolnenie=0;
	int BichKard=1000;
	int BichWallet=0;

	int MidKard=5000;
	int MidWallet=0;

	int TopKard=20000;
	int TopWallet=0;
	
	int price = 0, timeArend, priceArend;
	

	bool work = true;
	while (work)
	{
		system("cls");

		cout << "Добро пожаловать в Яндекс.Суета, введите имя и возраст и пароль чтобы продолжить... \n";
		cout << "Имя(только английское): ";
		cin >> name;
		cout << "Пароль: ";
		cin >> inPassword;
		cout << "Возраст: ";
		cin >> inAge;
		
		while (work)
		{

			cout << "Введите пароль" << endl;
			cin >> Password;
			if (Password==inPassword||newPassword==Password)
			{
				while (work)
				{
				


					system("cls");
					if (inAge <= 21)
					{
						lvl = 1;
						cout << "Добро пожаловать " << name <<endl<< "Ваш уровень доверия: " << lvl << endl << "Вам доступен транспорт из раздела: Поминутный нищеброд" << endl;
						cout << "У тебя на счету: "<<BichWallet << endl;
						cout << "1. Взять машину в аренду\n";
						cout << "2. Правила пользования \n";
						cout << "3. Оснащение пушки-гонки \n";
						cout << "4. Пополнить кошелек \n";
					}
					else if (21 < inAge < 25)
					{
						lvl = 2;
						cout << "Добро пожаловать " << name << "\nВаш уровень доверия: " << lvl << "\nВам доступен транспорт из раздела: Районный хасанщик" << endl;
						cout << "У тебя на счету: " << MidWallet << endl;
						cout << "1. Взять машину в аренду\n";
						cout << "2. Правила пользования \n";
						cout << "3. Оснащение пушки-гонки \n";
						cout << "4. Пополнить кошелек \n";


					}
					else if (25 <= inAge)
					{
						lvl = 3;
						cout << "Добро пожаловать " << name << "\nВаш уровень доверия: " << "Вам доступен транспорт из раздела: Кашерный суетолог" << endl;
						cout << "У тебя на счету: " << TopWallet << endl;
						cout << "1. Взять машину в аренду\n";
						cout << "2. Правила пользования \n";
						cout << "3. Оснащение пушки-гонки \n";
						cout << "4. Пополнить кошелек \n";
					}
					if (lvl == 1)
					{


						cin >> d;

						switch (d)
						{

						case 1:
							system("cls");
							cout << "------------------------------Поминутный нищеброд------------------------------\n";
							cout << "Вам доступны такие авто как: ВАЗ 2101-2107, 2108-21099\n";
							cout << "1. Цена аренды:150р/час Выбрать машинку ваз 2101-2107 \n";
							cout << "2. Цена аренды:200р/час Выбрать машинку ваз 2108-21099 \n";
							cin >> c;
							switch (c)
							{
							case 1:
								system("cls");
								cout << "введите время на которое вы хотите взять машину: \n";
								cin >> timeArend;
								
								priceArend = 150;
								price = priceArend * timeArend;
								if (BichWallet>=price)
								{
									BichWallet = BichWallet - price;
									cout << "С вашего баланса было списано: " << price << endl;
									cout << "маладец, выбрал ссаную жигу которая никуда не едет, ей цена 20к, чисто въ**ать и в митол сдать\n";
									bichPriz = bichBonus[rand() % 2];
									cout << "Вам бонусом выпалo: " << bichPriz << "\n";
									system("pause\n");
								}
								else 
								{
									system("cls");
									cout << "У вас недостаточно средст на счету чтобы взять машину";
									system("pause\n");
								}
								break;

							case 2:
								system("cls");
								cout << "введите время на которое вы хотите взять машину: \n";
								cin >> timeArend;

								priceArend = 200;
								price = priceArend * timeArend;
								if (BichWallet >= price)
								{
									BichWallet = BichWallet - price;
									cout << "С вашего баланса было списано: " << price << endl;
									cout << "маладец, выбрал зубило, ну российский порш, сказать больше нечего, +уважение парней с района\n";
									bichPriz = bichBonus[rand() % 2];
									cout << "Вам бонусом выпалo: " << bichPriz << "\n";
									system("pause\n");
								}
								else
								{
									system("cls");
									cout << "У вас недостаточно средст на счету чтобы взять машину";
									system("pause\n");
								}
								break;
							}
							break;

						case 2:
							system("cls");
							cout << "Правила пользования: 1. Главное правило - правил нет.\n 2. Если встречная полоса свободна, почему бы не ехать по ней?\n 3. Будь загадочным, не включай поворотник.\n 4. Увидел кента - резко тормозни посреди дороги и спроси как он. \n5. Стоя на обочине, сперва открой дверь, а потом уже смотри едет ли кто. \n6. Если идет грамотная бикса - пропусти. \n7. Если тебя подрезали - догони, подрежь и посмотри дерзко. если увидел в ответ такой же взгляд - маякни чтобы открыл окно и спроси - ТЫ ЧЁ ОБОСТРИТЬ ХОЧЕШЬ? \n8. Если пришла смс, обязательно ответь за рулём, при этом едь 20-40 км/ч и виляй из ряда в ряд. \n9. Полосы нарисованы для красоты, не обязательно ехать в одном ряду. \n10. Если у тебя механика и зазвонил телефон - обязательно ответь и попроси кента переключать скорости. \n11. Увидел гаишника, обгони и посмотри с улыбкой, почувствуй своё превосходство. \n12. Если на светофоре кто-то снисходительно посмотрел на твою четырку - стартани с места, покажи у кого на самом деле крутая тачка. \n13. Если тебе надо повернуть налево - заранее прими правый ряд и поворачивай оттуда. \n14. Зеленый общий, красный наш. \n15. Тормози обязательно резко, предварительно хорошо разогнавшись. \n16. Ни в коем случае не держи дистанцию, залезь в зад машине, будто ты ее преследуешь! \n17. Увидел красивых девушек-посигналь. уверен в себе - подмигни. \n18. Остановили менты - приколи что спешишь на похороны/за лекарствами/на свадьбу/сын родился/на кипиш к пацанам. \n19. Паркуйся где в кайф, мы - свободные люди. \n20. Наклей тонировку, сняли - наклей еще раз. надоели снимать -повесь занавески с хаты. \n21.Заглох при кентах уезжай с пробуксовкой,возможно на второй,реабилитируйся. \n22. Включай музыку на максимум. пусть другие тоже насладятся творчеством Муцураева или старым рэпом. \n23. Высадив кентов - обязательно посигналь на прощание. \n24. Вози всегда в машине нож, скатерть и одноразовые стаканчики. ведь никогда не знаешь где и когда забухаешь. \n25. В машине должен быть освежитель воздуха - как минимум ёлочка. \n26. Знай фамилию хотя бы одного фсбшника и пугай гаишников, что можешь ему набрать, но не хочешь тревожить. \n27. Купи блатные номера, пусть даже они дороже твоей машины. \n28. Утром у многих начинается с пробежки, душа, завтрака. но это для слабаков. твое утро начинается с губки и шланга! \n29. Не забудь сказать на мойке, чтобы зачернили резину! \n30. Едешь с Мадиной - скачи из ряда в ряд со спокойным лицом на расслабоне, даже если у самого очко играет \n ";
							system("pause\n");
							break;
						case 3:
							system("cls");
							cout << "Раздел “ Поминутный нищеброд ” – в этом разделе вы можете арендовать марки российского автопрома низкого класса(ВАЗ 2101-2107, 2108-21099), в комплект входит тонировка в круг, ФСО, качёвая музыкаена флешке в бардачке, есть шанс что бонусом будет лежать в бардачке 100 на бенз или номера “Свои” в багажнике. \n\n Раздел “ районный хасанщик” – здесь авто классом повыше, всякие гранты, приоры, весты, поло, солярисы, ну ты понял короче, здесь уже набор побогаче, есть ФСО в два этажа, так же пятак в круг, мигалки под стекло, откидные номерные рамки.\n \n Раздел “кашерный суетолог” – Бэха 520 с шильдиками и обвесом М, камни 3.5 в китайском обвесе, ешка 1.8 с амг шильдиками и обвесом китайским, камаро на попель моторе экобуст. Тут полный фарш, ФСО, тонер, сгу, шторки на номерах, номерные рамки ФСО РФ, мигалки, рация настроенная на милицескую волну.";
							system("pause\n");
							break;
						case 4:
							system("cls");
							cout << "Баланс карты:"<<BichKard<<endl;
							cout << "На какую сумму хотите пополнить?\n";
							cin >> popolnenie;
							if (popolnenie <= BichKard)
							{
								system("cls");
								BichKard = BichKard - popolnenie;
								BichWallet = BichWallet + popolnenie;
								cout << "Деньги успешно зачислены на счёт\n";
							}
							else
							{
								system("cls");
								cout << "не хватает денег на счету\n";
								popolnenie = 0;
								system("pause\n");
							}
							system("pause\n");
						}
					}

					if (lvl == 2)
					{

						cin >> d;
						switch (d)
						{

						case 1:
							system("cls");
							cout << "------------------------------Районный хасанщик------------------------------\n";
							cout << "Вам доступны такие авто как: гранты, приоры, весты, поло, солярисы, ну ты понял короче\n";
							cout << "1. Цена аренды:700р/час Выбрать пацанскую прио  \n";
							cout << "2. Цена аренды:900р/час Выбрать кредитотошнотку \n";
							cin >> c;
							switch (c)
							{
							case 1:
								system("cls");
								cout << "введите время на которое вы хотите взять машину: \n";
								cin >> timeArend;

								priceArend = 700;
								price = priceArend * timeArend;
								if (MidWallet >= price)
								{
									MidWallet = MidWallet - price;
									cout << "С вашего баланса было списано: " << price << endl;
									cout << "+УВАЖЕНИЕ пацанов с района, ведь прио как 09 в девяностых, такая же бандитская, чисто для наведения пыли пагораду\n";
									midPriz = midBonus[rand() % 4];
									cout << "Вам бонусом выпалo: " << midPriz << "\n";
									system("pause\n");
								}
								else
								{
									system("cls");
									cout << "У вас недостаточно средст на счету чтобы взять машину";
									system("pause\n");
								}
								break;
							case 2:
								system("cls");
								cout << "введите время на которое вы хотите взять машину: \n";
								cin >> timeArend;

								priceArend = 900;
								price = priceArend * timeArend;
								if (MidWallet >= price)
								{
									MidWallet = MidWallet - price;
									cout << "С вашего баланса было списано: " << price << endl;
									cout << "Ну теперь все пацаны будут думать что ты взял кредит и ты будешь в их глазах казаться семьянином, ведь далеко не каждый может себе позволить весту или поло в кредит\n";
									midPriz = midBonus[rand() % 4];
									cout << "Вам бонусом выпалo: " << midPriz << "\n";
									system("pause\n");
								}
								else
								{
									system("cls");
									cout << "У вас недостаточно средст на счету чтобы взять машину";
									system("pause\n");
								}
								break;
							}
							
						case 2:
							system("cls");
							cout << "Правила пользования: 1. Главное правило - правил нет.\n 2. Если встречная полоса свободна, почему бы не ехать по ней?\n 3. Будь загадочным, не включай поворотник.\n 4. Увидел кента - резко тормозни посреди дороги и спроси как он. \n5. Стоя на обочине, сперва открой дверь, а потом уже смотри едет ли кто. \n6. Если идет грамотная бикса - пропусти. \n7. Если тебя подрезали - догони, подрежь и посмотри дерзко. если увидел в ответ такой же взгляд - маякни чтобы открыл окно и спроси - ТЫ ЧЁ ОБОСТРИТЬ ХОЧЕШЬ? \n8. Если пришла смс, обязательно ответь за рулём, при этом едь 20-40 км/ч и виляй из ряда в ряд. \n9. Полосы нарисованы для красоты, не обязательно ехать в одном ряду. \n10. Если у тебя механика и зазвонил телефон - обязательно ответь и попроси кента переключать скорости. \n11. Увидел гаишника, обгони и посмотри с улыбкой, почувствуй своё превосходство. \n12. Если на светофоре кто-то снисходительно посмотрел на твою четырку - стартани с места, покажи у кого на самом деле крутая тачка. \n13. Если тебе надо повернуть налево - заранее прими правый ряд и поворачивай оттуда. \n14. Зеленый общий, красный наш. \n15. Тормози обязательно резко, предварительно хорошо разогнавшись. \n16. Ни в коем случае не держи дистанцию, залезь в зад машине, будто ты ее преследуешь! \n17. Увидел красивых девушек-посигналь. уверен в себе - подмигни. \n18. Остановили менты - приколи что спешишь на похороны/за лекарствами/на свадьбу/сын родился/на кипиш к пацанам. \n19. Паркуйся где в кайф, мы - свободные люди. \n20. Наклей тонировку, сняли - наклей еще раз. надоели снимать -повесь занавески с хаты. \n21.Заглох при кентах уезжай с пробуксовкой,возможно на второй,реабилитируйся. \n22. Включай музыку на максимум. пусть другие тоже насладятся творчеством Муцураева или старым рэпом. \n23. Высадив кентов - обязательно посигналь на прощание. \n24. Вози всегда в машине нож, скатерть и одноразовые стаканчики. ведь никогда не знаешь где и когда забухаешь. \n25. В машине должен быть освежитель воздуха - как минимум ёлочка. \n26. Знай фамилию хотя бы одного фсбшника и пугай гаишников, что можешь ему набрать, но не хочешь тревожить. \n27. Купи блатные номера, пусть даже они дороже твоей машины. \n28. Утром у многих начинается с пробежки, душа, завтрака. но это для слабаков. твое утро начинается с губки и шланга! \n29. Не забудь сказать на мойке, чтобы зачернили резину! \n30. Едешь с Мадиной - скачи из ряда в ряд со спокойным лицом на расслабоне, даже если у самого очко играет \n ";
							system("pause\n");
							break;
						case 3:
							system("cls");
							cout << "Раздел “ Поминутный нищеброд ” – в этом разделе вы можете арендовать марки российского автопрома низкого класса(ВАЗ 2101-2107, 2108-21099), в комплект входит тонировка в круг, ФСО, качёвая музыкаена флешке в бардачке, есть шанс что бонусом будет лежать в бардачке 100 на бенз или номера “Свои” в багажнике. \n\n Раздел “ районный хасанщик” – здесь авто классом повыше, всякие гранты, приоры, весты, поло, солярисы, ну ты понял короче, здесь уже набор побогаче, есть ФСО в два этажа, так же пятак в круг, мигалки под стекло, откидные номерные рамки.\n \n Раздел “кашерный суетолог” – Бэха 520 с шильдиками и обвесом М, камни 3.5 в китайском обвесе, ешка 1.8 с амг шильдиками и обвесом китайским, камаро на попель моторе экобуст. Тут полный фарш, ФСО, тонер, сгу, шторки на номерах, номерные рамки ФСО РФ, мигалки, рация настроенная на милицескую волну.";
							system("pause\n");
							break;
						case 4:
							system("cls");
							cout << "Баланс карты:" << MidKard << endl;
							cout << "На какую сумму хотите пополнить?\n";
							cin >> popolnenie;
							if (popolnenie <= MidKard)
							{
								system("cls");
								MidKard = MidKard - popolnenie;
								MidWallet = MidWallet + popolnenie;
								cout << "Деньги успешно зачислены на счёт\n";
							}
							else
							{
								system("cls");
								cout << "не хватает денег на счету\n";
								popolnenie = 0;
								system("pause\n");
							}

						}
					}
					if (lvl == 3)
					{

						cin >> d;
						switch (d)
						{
						case 1:
							system("cls");
							cout << "------------------------------Кашерный суетолог------------------------------\n";
							cout << "Вам доступны такие авто как: Бэха 520 с шильдиками и обвесом М, камни 3.5 в китайском обвесе, ешка 1.8 с амг шильдиками и обвесом китайским, камаро на попель моторе экобуст\n";
							cout << "1. Цена аренды: 1700р/час Выбрать машинку БэЭмВэ, камни или чевролет \n";
							cout << "2. Цена аренды: 2500р/часВыбрать мэрцэдэс \n";
							cin >> c;
							switch (c)
							{
							case 1:
								system("cls");
								cout << "введите время на которое вы хотите взять машину: \n";
								cin >> timeArend;

								priceArend = 1700;
								price = priceArend * timeArend;
								if (TopWallet >= price)
								{
									TopWallet = TopWallet - price;
									cout << "С вашего баланса было списано: " << price << endl;
									cout << "Мка быстрее, но Ешка солиднее братан, камни для дидов, а камаро на опель моторе вообще непонятно для кого\n";
									topPriz = topBonus[rand() % 5];
									cout << "Вам бонусом выпалo: " << topPriz << "\n";
									system("pause\n");
								}
								else
								{
									system("cls");
									cout << "У вас недостаточно средст на счету чтобы взять машину";
									system("pause\n");
								}
								break;
							case 2:
								system("cls");
								cout << "введите время на которое вы хотите взять машину: \n";
								cin >> timeArend;

								priceArend = 2500;
								price = priceArend * timeArend;
								if (TopWallet >= price)
								{
									TopWallet = TopWallet - price;
									cout << "С вашего баланса было списано: " << price << endl;
									cout << "Вай какую соску выбрал, АМГ она да? Без мам пап и кредитов получается?\n";
									topPriz = topBonus[rand() % 5];
									cout << "Вам бонусом выпалo: " << topPriz << "\n";
									system("pause\n");
								}
								else
								{
									system("cls");
									cout << "У вас недостаточно средст на счету чтобы взять машину";
									system("pause\n");
								}
								break;
							}
							break;
						case 2:
							system("cls");
							cout << "Правила пользования: 1. Главное правило - правил нет.\n 2. Если встречная полоса свободна, почему бы не ехать по ней?\n 3. Будь загадочным, не включай поворотник.\n 4. Увидел кента - резко тормозни посреди дороги и спроси как он. \n5. Стоя на обочине, сперва открой дверь, а потом уже смотри едет ли кто. \n6. Если идет грамотная бикса - пропусти. \n7. Если тебя подрезали - догони, подрежь и посмотри дерзко. если увидел в ответ такой же взгляд - маякни чтобы открыл окно и спроси - ТЫ ЧЁ ОБОСТРИТЬ ХОЧЕШЬ? \n8. Если пришла смс, обязательно ответь за рулём, при этом едь 20-40 км/ч и виляй из ряда в ряд. \n9. Полосы нарисованы для красоты, не обязательно ехать в одном ряду. \n10. Если у тебя механика и зазвонил телефон - обязательно ответь и попроси кента переключать скорости. \n11. Увидел гаишника, обгони и посмотри с улыбкой, почувствуй своё превосходство. \n12. Если на светофоре кто-то снисходительно посмотрел на твою четырку - стартани с места, покажи у кого на самом деле крутая тачка. \n13. Если тебе надо повернуть налево - заранее прими правый ряд и поворачивай оттуда. \n14. Зеленый общий, красный наш. \n15. Тормози обязательно резко, предварительно хорошо разогнавшись. \n16. Ни в коем случае не держи дистанцию, залезь в зад машине, будто ты ее преследуешь! \n17. Увидел красивых девушек-посигналь. уверен в себе - подмигни. \n18. Остановили менты - приколи что спешишь на похороны/за лекарствами/на свадьбу/сын родился/на кипиш к пацанам. \n19. Паркуйся где в кайф, мы - свободные люди. \n20. Наклей тонировку, сняли - наклей еще раз. надоели снимать -повесь занавески с хаты. \n21.Заглох при кентах уезжай с пробуксовкой,возможно на второй,реабилитируйся. \n22. Включай музыку на максимум. пусть другие тоже насладятся творчеством Муцураева или старым рэпом. \n23. Высадив кентов - обязательно посигналь на прощание. \n24. Вози всегда в машине нож, скатерть и одноразовые стаканчики. ведь никогда не знаешь где и когда забухаешь. \n25. В машине должен быть освежитель воздуха - как минимум ёлочка. \n26. Знай фамилию хотя бы одного фсбшника и пугай гаишников, что можешь ему набрать, но не хочешь тревожить. \n27. Купи блатные номера, пусть даже они дороже твоей машины. \n28. Утром у многих начинается с пробежки, душа, завтрака. но это для слабаков. твое утро начинается с губки и шланга! \n29. Не забудь сказать на мойке, чтобы зачернили резину! \n30. Едешь с Мадиной - скачи из ряда в ряд со спокойным лицом на расслабоне, даже если у самого очко играет \n ";
							system("pause\n");
							break;
						case 3:
							system("cls");
							cout << "Раздел “ Поминутный нищеброд ” – в этом разделе вы можете арендовать марки российского автопрома низкого класса(ВАЗ 2101-2107, 2108-21099), в комплект входит тонировка в круг, ФСО, качёвая музыкаена флешке в бардачке, есть шанс что бонусом будет лежать в бардачке 100 на бенз или номера “Свои” в багажнике. \n\n Раздел “ районный хасанщик” – здесь авто классом повыше, всякие гранты, приоры, весты, поло, солярисы, ну ты понял короче, здесь уже набор побогаче, есть ФСО в два этажа, так же пятак в круг, мигалки под стекло, откидные номерные рамки.\n \n Раздел “кашерный суетолог” – Бэха 520 с шильдиками и обвесом М, камни 3.5 в китайском обвесе, ешка 1.8 с амг шильдиками и обвесом китайским, камаро на попель моторе экобуст. Тут полный фарш, ФСО, тонер, сгу, шторки на номерах, номерные рамки ФСО РФ, мигалки, рация настроенная на милицескую волну.";
							system("pause\n");
							break;
						case 4:
							system("cls");
							cout << "Баланс карты:" << TopKard << endl;
							cout << "На какую сумму хотите пополнить?\n";
							cin >> popolnenie;
							if (popolnenie <= TopKard)
							{
								system("cls");
								TopKard = TopKard - popolnenie;
								TopWallet = TopWallet + popolnenie;
								cout << "Деньги успешно зачислены на счёт\n";
								system("pause\n");
							}
							else
							{
								system("cls");
								cout << "не хватает денег на счету\n";
								popolnenie = 0;
								system("pause\n");
							} 
						
						}

					}
				}
			}
			else
			{
				system("cls");
				cout << "Неверный пароль \n 1. ДА \n 2. НЕТ";
				cin >> a;
				switch (a)
				{
				case 1:
					system("cls");
					cout << "Введите новый пароль ";
					cin >> newPassword;
					Password = newPassword;
					system("cls");
					cout << "Ваш пароль успешно сменён... ";
					system("pause\n");
					break;
				case 2:
					cout << "Ну ты внатуре дебил, твой пароль\n"<<inPassword<<endl;
					system("pause\n");
					break;
				default:
					break;
				}
				
			}

		}

	}
}
