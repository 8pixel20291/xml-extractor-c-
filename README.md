 StreamReader reader = new StreamReader(@"C:\Users\DearUser\Desktop\pubmed24n1218.xml");
            string txt2 = reader.ReadToEnd();
            reader.Close();
            //var doc = new XmlDocument();
            //doc.Load(@"C:\Users\DearUser\Desktop\test.xml");
            XDocument doc2 = XDocument.Parse(txt2);

            foreach (var doi in doc2.Descendants("ELocationID"))
            {

                if (doi.ToString().Contains("doi"))
                {
                    using (StreamWriter sw1 = File.AppendText(@"F:\corner\export-selenium-txt\pubabstract\test.txt"))
                    {
                        sw1.WriteLine(doi.Value + " vvvvvvvvvvvvvvvvvvvv");
                    }
                    using (StreamWriter sw1 = File.AppendText(@"F:\corner\export-selenium-txt\pubabstract\test2.txt"))
                    {
                        sw1.WriteLine(doi.ToString() + " vvvvvvvvvvvvvvvvvvvv");
                    }
                }
                             
            }
            http://www.8pixel.ir/
