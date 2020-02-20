Lab1, Exercise 3

![](media/5dc9d033053f2f366729fb6fde8559f9.png)

![](media/1c2dea1e35e7823e580cc8a895376eba.png)

![](media/a193bbe4ddc6b5686adf19509c282b6a.png)

NOT QUERY PARAMETERS!!!!

Do Query parameters here!!! then create a function

![](media/07c03b74df2c505eb64deaa91ce61696.png)

![](media/8552799840c87c8ba77fec3dbaf712ec.png)

![](media/b76710c2fabc0dc8900c8573ef742e7e.png)

![](media/9403eb10f89cdd3b28ed283b45f8e18e.png)

![](media/8f518e3fafe0df2a687f97f54f7abba3.png)

![](media/536facaa0943331674ad40b2a71d2437.png)

![](media/d673cd8bdda2502bb51e191e3a7cdbed.png)

![](media/a0fd8795421a3cb92f9168520ac689ee.png)

![](media/411e75ded2abf24740f0d724da8b8425.png)

![](media/1c7ff60848980b6558e7af2845efe2dc.png)

let

Source = Sql.Database("sqlazuredw001.database.windows.net", "AdventureWorksDW",
[Query="EXEC getProductSalesByCategory '" & \@Category & "'"])

in

Source

Query is correct, it’s the privacy settings that mess it up, let’s see if we can
fix it, properly

![](media/299388be3189f8732e22cc06d20a477b.png)

![](media/2e0ba2cdccd98ff98567736ea6c402a4.png)

![](media/fbf1954d2a47e7481df533fef83c3210.png)

![](media/ceedf459719fbf97cbc7e8da56860994.png)

![](media/6acf800685861fd3c67fcecd6c1bde96.png)

![](media/fb39c82bd2847110516446ae0b2dbee0.png)

![](media/9c302e2f073c677756ea78759299da22.png)

![](media/33690e1cf24399a471c9c8483404848c.png)
