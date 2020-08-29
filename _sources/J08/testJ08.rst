Квиз
---------

.. mchoice:: Тест12_Питање1
   :answer_a: ocene1["ProsekUc"] = 0.0
   :answer_b: ocene1[ProsekUc] = 0.0
   :answer_c: ocene1.loc["ProsekUc"] = 0.0
   :answer_d: ocene1.ProsekUc = 0.0
   :correct: a
   :feedback_a: Тачно!
   :feedback_b: Покушај поново!
   :feedback_c: Покушај поново!
   :feedback_d: Покушај поново!

   Погледај пажљиво следећи Пајтон програм

   .. code-block:: python

      import pandas as pd
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
      ocene = pd.DataFrame(razred)
      ocene.columns=["Ime", "Informatika", "Engleski", "Matematika", "Fizika", "Hemija", "Likovno"]
      ocene1 = ocene.set_index("Ime")

   па означи наредбу која табели ``ocene1`` додаје нову колону ``ProsekUc``:

.. mchoice:: Тест12_Питање2
   :answer_a: ocene1["ProsekPr"] = 0.0
   :answer_b: ocene1[ProsekPr] = 0.0
   :answer_c: ocene1.loc["ProsekPr"] = 0.0
   :answer_d: ocene1.ProsekPr = 0.0
   :correct: c
   :feedback_a: Покушај поново!
   :feedback_b: Покушај поново!
   :feedback_c: Тачно!
   :feedback_d: Покушај поново!

   Погледај пажљиво Пајтон програм у претходном задатку
   па означи наредбу која табели ``ocene1`` додаје нову врсту ``ProsekPr``:

.. mchoice:: Тест12_Питање3
   :answer_a: Овај програм снима учитане податке на удаљени ресурс (интернет) у формату HTML.
   :answer_b: Овај програм снима учитане податке на удаљени ресурс (интернет) у формату CSV.
   :answer_c: Овај програм снима учитане податке на рачунар на коме се програм извршава.
   :answer_d: Овај програм снима учитане податке на рачунар на коме се програм извршава у формату CSV.
   :correct: d
   :feedback_a: Покушај поново!
   :feedback_b: Покушај поново!
   :feedback_c: Покушај поново!
   :feedback_d: Тачно!

   Погледај пажљиво следећи Пајтон програм

   .. code-block:: python

      import pandas as pd
      US = pd.read_html("https://simple.wikipedia.org/wiki/List_of_U.S._states", header=[0,1])[0]
      US.to_csv("podaci/SAD.csv")

   па означи исказ који садржи навише тачних информација (*само један*):

.. mchoice:: Тест12_Питање4
   :answer_a: Овај програм снима учитане податке на удаљени ресурс (интернет) у формату CSV.
   :answer_b: Овај програм снима учитане податке на рачунар на коме се програм извршава у формату CSV.
   :answer_c: Овај програм снима учитане податке на рачунар на коме се програм извршава у формату CSV и при томе у датотеку записује и садржај индексне колоне.
   :answer_d: Овај програм снима учитане податке на рачунар на коме се програм извршава у формату CSV и при томе у датотеку не записује садржај индексне колоне.
   :correct: d
   :feedback_a: Покушај поново!
   :feedback_b: Покушај поново!
   :feedback_c: Покушај поново!
   :feedback_d: Тачно!

   Погледај пажљиво следећи Пајтон програм

   .. code-block:: python

      import pandas as pd
      drzave = pd.read_csv("https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv")
      drzave.to_csv("podaci/drzavesveta.csv", index=False)

   па означи исказ који садржи навише тачних информација (*само један*):
