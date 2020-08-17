Тест
---------

.. mchoice:: Тест13_Питање1
   :answer_a: tabela2 = tabela1.sort_values(by="Visina")
   :answer_b: tabela2 = tabela1.sort_values("Visina")
   :answer_c: tabela2 = tabela1.sort(by="Visina")
   :answer_d: tabela2 = tabela1.sort("Visina")
   :correct: a
   :feedback_a: Тачно!
   :feedback_b: Покушај поново!
   :feedback_c: Покушај поново!
   :feedback_d: Покушај поново!

   На слици су дате две табеле, лево је ``tabela1``, а десно ``tabela2``:

   .. image:: ../../_images/test2813sl1.png
      :width: 600

   Означи наредбу којом се од табеле ``tabela1`` добија ``tabela2``.
   
.. mchoice:: Тест13_Питање2
   :answer_a: tabela3 = tabela1.sort_values(by="Visina", ascending=False)
   :answer_b: tabela3 = tabela1.sort_values("Visina", descending=False)
   :answer_c: tabela3 = tabela1.sort(by="Visina", ascending=False)
   :answer_d: tabela3 = tabela1.sort("Visina", descending=False)
   :correct: a
   :feedback_a: Тачно!
   :feedback_b: Покушај поново!
   :feedback_c: Покушај поново!
   :feedback_d: Покушај поново!

   На слици су дате две табеле, лево је ``tabela1``, а десно ``tabela3``:

   .. image:: ../../_images/test2813sl2.png
      :width: 600

   Означи наредбу којом се од табеле ``tabela1`` добија ``tabela3``.

.. mchoice:: Тест13_Питање3
   :answer_a: tabela1
   :answer_b: tabela2
   :answer_c: tabela3
   :answer_d: Ништа од понуђеног.
   :correct: c
   :feedback_a: Покушај поново!
   :feedback_b: Покушај поново!
   :feedback_c: Тачно!
   :feedback_d: Покушај поново!

   На слици су дате три табеле, лево је ``tabela1``, у средини је ``tabela2``, а десно је ``tabela3``:

   .. image:: ../../_images/test2813sl4.png
      :width: 600

   Шта треба уписати уместо три упитника у програму:
   
   .. code-block:: text
   
      import matplotlib.pyplot as plt
      plt.figure(figsize=(10,5))
      plt.bar(???.index, ???["Visina"], label="Visina")
      plt.bar(???.index, ???["Masa"], label="Masa")
      plt.title("Visina i masa dece u grupi")
      plt.legend()
      plt.show()
      plt.close()
     
   да би он нацртао следећи дијаграм:

   .. image:: ../../_images/test2813sl3.png
      :width: 600

.. mchoice:: Тест13_Питање4
   :answer_a: tabela4 = tabela1[tabela1.Pol == "ž"]
   :answer_b: tabela4 = tabela1[Pol == "ž"]
   :answer_c: tabela4 = tabela1["ž"]
   :answer_d: Ништа од понуђеног.
   :correct: a
   :feedback_a: Тачно!
   :feedback_b: Покушај поново!
   :feedback_c: Покушај поново!
   :feedback_d: Покушај поново!

   На слици су дате две табеле, лево је ``tabela1``, а десно ``tabela4``:

   .. image:: ../../_images/test2813sl5.png
      :width: 600

   Означи наредбу којом се од табеле ``tabela1`` добија ``tabela4``.

.. mchoice:: Тест13_Питање5
   :answer_a: tabela5 = tabela1[tabela1.Pol > 50]
   :answer_b: tabela5 = tabela1[Masa == "ž"]
   :answer_c: tabela5 = tabela1[tabela1.Masa == 50]
   :answer_d: tabela5 = tabela1[tabela1.Masa < 50]
   :answer_e: Ништа од понуђеног.
   :correct: e
   :feedback_a: Покушај поново!
   :feedback_b: Покушај поново!
   :feedback_c: Покушај поново!
   :feedback_d: Покушај поново!
   :feedback_e: Тачно!

   На слици су дате две табеле, лево је ``tabela1``, а десно ``tabela5``:

   .. image:: ../../_images/test2813sl6.png
      :width: 600

   Означи наредбу којом се од табеле ``tabela1`` добија ``tabela5``.

.. mchoice:: Тест13_Питање6
   :answer_a: tabela1[(tabela1.Masa <= 55) & (tabela1.Pol == "m")]
   :answer_b: tabela1[tabela1.Masa <= 55 & tabela1.Pol == "m"]
   :answer_c: tabela1[(Masa <= 55) & (Pol == "m")]
   :answer_d: tabela1[Masa <= 55 & Pol == "m"]
   :correct: a
   :feedback_a: Тачно!
   :feedback_b: Покушај поново!
   :feedback_c: Покушај поново!
   :feedback_d: Покушај поново!

   На слици су дати табела ``tabela1`` и дијаграм:

   .. image:: ../../_images/test2813sl7.png
      :width: 600

   Шта треба уписати уместо три упитника у програму:
   
   .. code-block:: text
   
      import matplotlib.pyplot as plt
      tabelica = ???
      plt.bar(tabelica.index, tabelica["Visina"], label="Visina")
      plt.bar(tabelica.index, tabelica["Masa"], label="Masa")
      plt.legend()
      plt.show()
      plt.close()
     
   да би он нацртао дијаграм који је дат поред табеле.

.. mchoice:: Тест13_Питање7
   :answer_a: tabela1.Starost.counts()
   :answer_b: tabela1[Starost].value_counts()
   :answer_c: tabela1[value="Starost"].counts()
   :answer_d: tabela1["Starost"].value_counts()
   :correct: d
   :feedback_a: Покушај поново!
   :feedback_b: Покушај поново!
   :feedback_c: Покушај поново!
   :feedback_d: Тачно!

   На слици су дати табела ``tabela1`` и дијаграм:

   .. image:: ../../_images/test2813sl8.png
      :width: 600

   Шта треба уписати уместо три упитника у програму:
   
   .. code-block:: text
   
      import matplotlib.pyplot as plt
      frekv = ???
      plt.pie(frekv.values, labels=frekv.index)
      plt.show()
      plt.close()
     
   да би он нацртао дијаграм који је дат поред табеле.
