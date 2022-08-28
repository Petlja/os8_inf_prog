Библиотека *pandas* и структура података *DataFrame*
----------------------------------------------------

.. technicalnote::

    Препоручујемо да ову лекцију покренеш на свом рачунару тако што ћеш у `фолдеру за рад офлајн <https://github.com/Petlja/VIII_prog_rev_radni/archive/refs/heads/main.zip>`_ покренути Џупитер свеску `Rad sa tabelama pomocu pandas biblioteke.ipynb` на начин на који је то објашњено у поглављу `Покретање Џупитер радних свески </J0A/J0A.html#jupyter>`_ у уводу овог приручника. 


За ефикасно манипулисање табеларно представљеним подацима у Пајтону
развијена је библиотека *pandas*. Њу можемо увести као што смо увозили и
остале библиотеке (и уз пут ћемо јој дати надимак да бисмо мање морали
да куцамо):

.. code:: ipython3

    import pandas as pd

Из ове библиотеке ћемо користити структуру података која се зове
*DataFrame* (енгл. *data* значи „подаци”, *frame* значи „оквир”, тако да
*DataFrame* значи „оквир са подацима”, односно „табела”).

Податке о деци сада лако можемо да препакујемо у *DataFrame* позивом
функције са истим именом:

.. code:: ipython3

    tabela = pd.DataFrame(podaci)

Претходна команда није дала никакав излаз. Она је просто препаковала
податке наведене у листи ``podaci`` у нову структуру података. Да бисмо
се уверили да се ради само о препакивању, исписаћемо садржај променљиве
``tabela``:

.. code:: ipython3

    tabela


.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>0</th>
          <th>1</th>
          <th>2</th>
          <th>3</th>
          <th>4</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>0</th>
          <td>Ana</td>
          <td>ž</td>
          <td>13</td>
          <td>46</td>
          <td>160</td>
        </tr>
        <tr>
          <th>1</th>
          <td>Bojan</td>
          <td>m</td>
          <td>14</td>
          <td>52</td>
          <td>165</td>
        </tr>
        <tr>
          <th>2</th>
          <td>Vlada</td>
          <td>m</td>
          <td>13</td>
          <td>47</td>
          <td>157</td>
        </tr>
        <tr>
          <th>3</th>
          <td>Gordana</td>
          <td>ž</td>
          <td>15</td>
          <td>54</td>
          <td>165</td>
        </tr>
        <tr>
          <th>4</th>
          <td>Dejan</td>
          <td>m</td>
          <td>15</td>
          <td>56</td>
          <td>163</td>
        </tr>
        <tr>
          <th>5</th>
          <td>Đorđe</td>
          <td>m</td>
          <td>13</td>
          <td>45</td>
          <td>159</td>
        </tr>
        <tr>
          <th>6</th>
          <td>Elena</td>
          <td>ž</td>
          <td>14</td>
          <td>49</td>
          <td>161</td>
        </tr>
        <tr>
          <th>7</th>
          <td>Žaklina</td>
          <td>ž</td>
          <td>15</td>
          <td>52</td>
          <td>164</td>
        </tr>
        <tr>
          <th>8</th>
          <td>Zoran</td>
          <td>m</td>
          <td>15</td>
          <td>57</td>
          <td>167</td>
        </tr>
        <tr>
          <th>9</th>
          <td>Ivana</td>
          <td>ž</td>
          <td>13</td>
          <td>45</td>
          <td>158</td>
        </tr>
        <tr>
          <th>10</th>
          <td>Jasna</td>
          <td>ž</td>
          <td>14</td>
          <td>51</td>
          <td>162</td>
        </tr>
      </tbody>
    </table>
    </div>



Ево и кратког видеа:

.. ytpopup:: _AJYNXq53hk
    :width: 735
    :height: 415
    :align: center

Да би табела била прегледнија, даћемо колонама име. Колонама се име даје
овако:

.. code:: ipython3

    tabela = pd.DataFrame(podaci)
    tabela.columns=["Ime", "Pol", "Starost", "Masa", "Visina"]
    tabela


.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>Ime</th>
          <th>Pol</th>
          <th>Starost</th>
          <th>Masa</th>
          <th>Visina</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>0</th>
          <td>Ana</td>
          <td>ž</td>
          <td>13</td>
          <td>46</td>
          <td>160</td>
        </tr>
        <tr>
          <th>1</th>
          <td>Bojan</td>
          <td>m</td>
          <td>14</td>
          <td>52</td>
          <td>165</td>
        </tr>
        <tr>
          <th>2</th>
          <td>Vlada</td>
          <td>m</td>
          <td>13</td>
          <td>47</td>
          <td>157</td>
        </tr>
        <tr>
          <th>3</th>
          <td>Gordana</td>
          <td>ž</td>
          <td>15</td>
          <td>54</td>
          <td>165</td>
        </tr>
        <tr>
          <th>4</th>
          <td>Dejan</td>
          <td>m</td>
          <td>15</td>
          <td>56</td>
          <td>163</td>
        </tr>
        <tr>
          <th>5</th>
          <td>Đorđe</td>
          <td>m</td>
          <td>13</td>
          <td>45</td>
          <td>159</td>
        </tr>
        <tr>
          <th>6</th>
          <td>Elena</td>
          <td>ž</td>
          <td>14</td>
          <td>49</td>
          <td>161</td>
        </tr>
        <tr>
          <th>7</th>
          <td>Žaklina</td>
          <td>ž</td>
          <td>15</td>
          <td>52</td>
          <td>164</td>
        </tr>
        <tr>
          <th>8</th>
          <td>Zoran</td>
          <td>m</td>
          <td>15</td>
          <td>57</td>
          <td>167</td>
        </tr>
        <tr>
          <th>9</th>
          <td>Ivana</td>
          <td>ž</td>
          <td>13</td>
          <td>45</td>
          <td>158</td>
        </tr>
        <tr>
          <th>10</th>
          <td>Jasna</td>
          <td>ž</td>
          <td>14</td>
          <td>51</td>
          <td>162</td>
        </tr>
      </tbody>
    </table>
    </div>



Када свака колона има своје име, можемо да приступимо појединачним
колонама:

.. code:: ipython3

    tabela["Ime"]




.. parsed-literal::

    0         Ana
    1       Bojan
    2       Vlada
    3     Gordana
    4       Dejan
    5       Đorđe
    6       Elena
    7     Žaklina
    8       Zoran
    9       Ivana
    10      Jasna
    Name: Ime, dtype: object



.. code:: ipython3

    tabela["Visina"]




.. parsed-literal::

    0     160
    1     165
    2     157
    3     165
    4     163
    5     159
    6     161
    7     164
    8     167
    9     158
    10    162
    Name: Visina, dtype: int64



Имена свих колона су увек доступна у облику листе овако:

.. code:: ipython3

    tabela.columns




.. parsed-literal::

    Index(['Ime', 'Pol', 'Starost', 'Masa', 'Visina'], dtype='object')



Функције за елементарну анализу табеларних података
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Кад су подаци сложени у *DataFrame*, помоћу следећих функција лако
можемо да вршимо елементарну анализу података у табели: - ``.sum()`` –
рачуна збир елемената у колони (сума); - ``.mean()`` – рачуна средњу
вредност елемената у колони; - ``.median()`` – рачуна медијану елемената
у колони; - ``.min()`` – рачуна најмању вредност у колони (минимум); -
``.max()`` – рачуна највећу вредност у колони (максимум).

Да видимо како то ради на примеру табеле ``tabela``. Конкретно, висину
најнижег детета у групи можемо да добијемо са:

.. code:: ipython3

    tabela["Visina"].min()




.. parsed-literal::

    157



Колико година има најстарије дете у групи?

.. code:: ipython3

    tabela["Starost"].max()




.. parsed-literal::

    15



Средња вредност висине деце у групи је:

.. code:: ipython3

    tabela["Visina"].mean()




.. parsed-literal::

    161.9090909090909



Медијална висина:

.. code:: ipython3

    tabela["Visina"].median()




.. parsed-literal::

    162.0



Рачун са колонама и редовима табеле
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Колико год било унапред дефинисаних функција за анализу података у
табели, то је ограничен број. Нама може да затреба нешто другачије. У
том случају ће бити потребно да напишемо програм који израчунава тражену
вредност. Овде ћемо приказати неке једноставне примере.

Кренимо од скупа података о оценама у једном разреду. У ћелији испод
дате су оцене неких ученика из информатике, енглеског, математике,
физике, хемије и ликовног:

.. code:: ipython3

    razred = [["Ana",     5, 3, 5, 2, 4, 5],
              ["Bojan",   5, 5, 5, 5, 5, 5],
              ["Vlada",   4, 5, 3, 4, 5, 4],
              ["Gordana", 5, 5, 5, 5, 5, 5],
              ["Dejan",   3, 4, 2, 3, 3, 4],
              ["Đorđe",   4, 5, 3, 4, 5, 4],
              ["Elena",   3, 3, 3, 4, 2, 3],
              ["Žaklina", 5, 5, 4, 5, 4, 5],
              ["Zoran",   4, 5, 4, 4, 3, 5],
              ["Ivana",   2, 2, 2, 2, 2, 5],
              ["Jasna",   3, 4, 5, 4, 5, 5]]

Сада ћемо од ових података направити табелу чије колоне ће се звати
*Ime*, *Informatika*, *Engleski*, *Matematika*, *Fizika*, *Hemija* и
*Likovno*.

.. code:: ipython3

    ocene = pd.DataFrame(razred)
    ocene.columns=["Ime", "Informatika", "Engleski", "Matematika", "Fizika", "Hemija", "Likovno"]
    ocene




.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>Ime</th>
          <th>Informatika</th>
          <th>Engleski</th>
          <th>Matematika</th>
          <th>Fizika</th>
          <th>Hemija</th>
          <th>Likovno</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>0</th>
          <td>Ana</td>
          <td>5</td>
          <td>3</td>
          <td>5</td>
          <td>2</td>
          <td>4</td>
          <td>5</td>
        </tr>
        <tr>
          <th>1</th>
          <td>Bojan</td>
          <td>5</td>
          <td>5</td>
          <td>5</td>
          <td>5</td>
          <td>5</td>
          <td>5</td>
        </tr>
        <tr>
          <th>2</th>
          <td>Vlada</td>
          <td>4</td>
          <td>5</td>
          <td>3</td>
          <td>4</td>
          <td>5</td>
          <td>4</td>
        </tr>
        <tr>
          <th>3</th>
          <td>Gordana</td>
          <td>5</td>
          <td>5</td>
          <td>5</td>
          <td>5</td>
          <td>5</td>
          <td>5</td>
        </tr>
        <tr>
          <th>4</th>
          <td>Dejan</td>
          <td>3</td>
          <td>4</td>
          <td>2</td>
          <td>3</td>
          <td>3</td>
          <td>4</td>
        </tr>
        <tr>
          <th>5</th>
          <td>Đorđe</td>
          <td>4</td>
          <td>5</td>
          <td>3</td>
          <td>4</td>
          <td>5</td>
          <td>4</td>
        </tr>
        <tr>
          <th>6</th>
          <td>Elena</td>
          <td>3</td>
          <td>3</td>
          <td>3</td>
          <td>4</td>
          <td>2</td>
          <td>3</td>
        </tr>
        <tr>
          <th>7</th>
          <td>Žaklina</td>
          <td>5</td>
          <td>5</td>
          <td>4</td>
          <td>5</td>
          <td>4</td>
          <td>5</td>
        </tr>
        <tr>
          <th>8</th>
          <td>Zoran</td>
          <td>4</td>
          <td>5</td>
          <td>4</td>
          <td>4</td>
          <td>3</td>
          <td>5</td>
        </tr>
        <tr>
          <th>9</th>
          <td>Ivana</td>
          <td>2</td>
          <td>2</td>
          <td>2</td>
          <td>2</td>
          <td>2</td>
          <td>5</td>
        </tr>
        <tr>
          <th>10</th>
          <td>Jasna</td>
          <td>3</td>
          <td>4</td>
          <td>5</td>
          <td>4</td>
          <td>5</td>
          <td>5</td>
        </tr>
      </tbody>
    </table>
    </div>



Ако желимо да израчунамо средње вредности оцена по предметима, треба на
сваку колону ове табеле (осим прве где су имена) да применимо функцију
``mean``. Листа са именима свих колона табеле ``ocene`` се добија као
``ocene.columns``, па сада само треба да прођемо кроз ову листу и за
сваку колону да израчунамо средњу вредност:

.. code:: ipython3

    predmeti=ocene.columns[1:]   # slajsom [1:] izdvajamo sve kolone sem prve
    for predmet in predmeti:
        print(predmet, "->", round(ocene[predmet].mean(), 2))


.. parsed-literal::

    Informatika -> 3.91
    Engleski -> 4.18
    Matematika -> 3.73
    Fizika -> 3.82
    Hemija -> 3.91
    Likovno -> 4.55
    

Да бисмо израчунали средње вредности по редовима, тј. за сваког ученика,
потребно је да уведемо нови начин приступа подацима у табели. Одређеном
реду табеле не можемо да приступимо без “аксесора”, посебних функција
писаних за објекте типа DataFrame, чији су аргументи имена редова/колона
или њихови индекси у угластим заградама. Аксесор, помоћу ког приступамо
редовима и појединачним елементима табеле је ``.iloc[]``. Аргументи овог
аксесора су нумерички индекси редова и колона који почињу од нуле.

На пример, податке из трећег реда (индекс је 2) табеле добијамо са:

.. code:: ipython3

    ocene.iloc[3]




.. parsed-literal::

    Ime            Gordana
    Informatika          5
    Engleski             5
    Matematika           5
    Fizika               5
    Hemija               5
    Likovno              5
    Name: 3, dtype: object



На овај начин смо добили податке за једног ученика, тј. ученицу.

Да бисмо из реда издвојили само нумеричке вредности, тј. оцене, потребно
је да аксесор добије и други аргумент. Осим индекса реда, потребно је да
ставимо и индексе колона. У овом примеру ћемо узети све индексе почевши
од индекса 1 јер име у колони са индексом нула.

.. code:: ipython3

    ocene.iloc[3,1:]




.. parsed-literal::

    Informatika    5
    Engleski       5
    Matematika     5
    Fizika         5
    Hemija         5
    Likovno        5
    Name: 3, dtype: object



Средње вредности оцена за све ученике сада можемо да израчунамо овако:

.. code:: ipython3

    for i in range(len(ocene)):
        print(ocene.iloc[i,0], "->", ocene.iloc[i,1:].mean())


.. parsed-literal::

    Ana -> 4.0
    Bojan -> 5.0
    Vlada -> 4.166666666666667
    Gordana -> 5.0
    Dejan -> 3.1666666666666665
    Đorđe -> 4.166666666666667
    Elena -> 3.0
    Žaklina -> 4.666666666666667
    Zoran -> 4.166666666666667
    Ivana -> 2.5
    Jasna -> 4.333333333333333
    
