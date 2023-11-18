# Averkin Alexander

- alexavkn@gmail.com
- +7 977 815-09-55
- Moscow, Guryanova st.

Specialist with 5+ years of experience. Capable of not only solving problems independently,
but also managing other programmers, as well as suggesting optimal ways to solve problems,
and factoring code.

## Skills

- Administration of 1C databases
- Understanding client-server architecture
- Writing exchanges using HTTP, web services, FTP
- Knowledge of the 1C programming language and built-in query language
- Resolving performance issues

### Code examples

- 1C

ВЫБРАТЬ РАЗРЕШЕННЫЕ
	Счет.Контрагент КАК Контрагент,
	Счет.Договор КАК Договор,
	Счет.ВалютаДокумента КАК ВалютаСчета,
	Счет.Договор.ВалютаРасчетов КАК ВалютаРасчетов,
	Счет.Ссылка КАК Счет,
	ОплатаСчетовИЗаказовОбороты.СуммаОборот КАК СуммаСчета,
	ОплатаСчетовИЗаказовОбороты.СуммаАвансаОборот КАК Предоплата,
	ОплатаСчетовИЗаказовОбороты.СуммаОплатыОборот КАК Оплата,
	ОплатаСчетовИЗаказовОбороты.СуммаАвансаОборот + ОплатаСчетовИЗаказовОбороты.СуммаОплатыОборот КАК Всего,
	ОплатаСчетовИЗаказовОбороты.СуммаОборот - ОплатаСчетовИЗаказовОбороты.СуммаОплатыОборот - ОплатаСчетовИЗаказовОбороты.СуммаАвансаОборот КАК ОсталосьОплатить,
	Счет.ВалютаДокумента КАК Валюта,
	Счет.Организация
ИЗ
	Документ.СчетНаОплату КАК Счет
		ЛЕВОЕ СОЕДИНЕНИЕ РегистрНакопления.ОплатаСчетовИЗаказов.Обороты({(&ПустаяДата)}, {(&ПустаяДата)}, Авто, {(СчетНаОплату.Организация) КАК Организация}) КАК ОплатаСчетовИЗаказовОбороты
		ПО Счет.Ссылка = ОплатаСчетовИЗаказовОбороты.СчетНаОплату,
	Константа.НациональнаяВалюта КАК НациональнаяВалюта
ГДЕ
	ВЫБОР
			КОГДА &КонецПериода = ДАТАВРЕМЯ(1, 1, 1)
				ТОГДА Счет.Дата >= &НачалоПериода
			ИНАЧЕ Счет.Дата МЕЖДУ &НачалоПериода И &КонецПериода
		КОНЕЦ
	И Счет.Проведен

- js

function multiply(a, b){
  return a * b;
}

const assert = require("chai").assert;

describe("Multiply", () => {
  it("fixed tests", () => {
    assert.strictEqual(multiply(1,1), 1);
    assert.strictEqual(multiply(2,1), 2);
    assert.strictEqual(multiply(2,2), 4);
    assert.strictEqual(multiply(3,5), 15);   
  });
});

## Experience

### <span>1C programmer, Sber</span> <span>Apr 2015 -- May 2016</span>
### <span>1C programmer, SOGAZ</span> <span>May 2016 -- now</span>

## Education

### <span>University of Managerment</span> <span>1995 -- 2000</span>

## Languages
- English - basic