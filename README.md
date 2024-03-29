# ქუიზი 5-6

მოცემული პროექტის მიზანია მოდელების შექმნა და შედეგების რაც შეიძლება მაღალი სიზუსტით პროგნოზირებ.
პროგრამა შესრულებულია python პროგრამირების ენისა და jupyter notebook-ის გამოყენებით. 

# მოდელები
შექმნილია 5 მოდელი:
* ერთ ცვლადიანი რეგრესიის;
* მრავალ ცვლადიანი რეგრესიის;
* გადაწყვეტილების ხის რეგრესიის;
* ლოგისტიკური რეგრესიის;
* გადაწყვეტილების ხის კლასიფიკაციის

# ერთ ცვლადიანი რეგრესიის მოდელი
მოდელის გამოყენებით საზამთროს წონის მიხედვით ვადგენთ მის ფასს.
აგებულია დიაგრამები:
* კორელაციების heatmap;
* წონისა და ფასის დამოკიდებულების scatter-ი;
* სატრენინგო მონაცემებისა და მისი წრფის აგება;
  
განხორციელდა დამოუკიდებელი და დამოკიდებული ცვლადები განცალკევება და შემდგომ მონაცემების დაყოფა სატრენინგოდ და სატესტოდ.
სატესტოს ზომად აღებულია 20%. ამის შემდგობ შეიქმნა მოდელი და მიეწდოა სატრენინგო მონაცემები. ამ მოდელის ეფექტურობა საკმაოდ მაღალია და წარმოადგენს 0.9947887877863348-ს.
შემდგომ განხორციელდა სატრენინგო მონაცემებისთვის შედეგის პროგნოზირება და ახალი მონაცემისთვის, კერძოდ 3.5 წონისს საზამთროსთვის ფასის პროგნიზირება.
დათასეთი შეგიძლიათ იხილოთ ბმულზე: https://www.kaggle.com/datasets/man526/watermelon-price-prediction-from-weight

# მრავალ ცვლადიანი რეგრესიის მოდელი 
სახლის მახასიათებლების მიხდევით უნდა მოვახდინოთ მისი ფასის პროგნოზირება მრავალ ცვლადიანი რეგრესიის მოდელის გამოყენებით.
წაშლილ იქნა სვეტი Address, შემოწმდა რომელიმე სვეტი ხომ არ არის null-ის შემცველი და აგებულ იქნა კორელაციების heatmap.
ამის შემდეგ განხორციელდა მონაცემების დაყოფა სატრენინგოდ და სატესტოდ. სატესტოს ზომად აღებულია 30%. მოდელის ეფექტურობა მაღალია და წარმოადგენს 0.9125718521857343.
დაბოლოს სატრენინგო მონაცემებისთვის მოხდა შედეგის პროგნოზირება და ახალი მონაცემისთვის (გარკვეული მახასიათბლების მქონე სახლისთვის) განხრციელდა ფასის პროგნოზირება.
დათასეთი შეგიძლიათ იხილოთ ბმულზე: https://www.kaggle.com/datasets/vikramamin/housing-linear-regression

# გადაწყვეტილების ხის რეგრესიის მოდელი
მოცემულია დეითასეთი წითელი ღვინის შესახებ და მოდელის მეშვეობით ხდება მისი ხარისხის პროგნოზირება.
ხარისხი იზომება რიცხვებში.
გამხორციელდა შემდგომი ეტაპები:
* შევამოწმოთ რომელიმე ჩანაწერში null ხომ არაა
* დამოკიდებული და დამოუკიდებელი სვეტების განცალკევება
* მონაცემების დაყოფა სატრენინგოდ და სატესტოდ. სატესტოს ზომად აღებულია 25%
* DecisionTreeRegressor მოდელის შექმნა სიღრმით 4 და სატრენინგო მონაცემებზე დატრენინგება
  
მოდელს აქვს საკმაოდ დაბალი სიზუსტე 0.36168043009244377. სატრენინგო მონაცემებისთვის მოხდა შედეგის პროგნოზირება და ახალი მონაცემისთვის, გარკვეული მახასიათებლების მქონე
წითელი ღვინისთვის ხარისხის პროგნოზირება.
დაბოლოს, მოდელის ექსპორტირება მოხდა tree_structure.dot ფაილად. შეგვიძლია ჩავსვათ ფაილის კონტენტი webgraphviz.com საიტზე, რათა ვიხილოთ დიაგრამა.

მოცემული დეითასეტი შეგიძლიათ იხილოთ ბმულზე https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009?select=winequality-red.csv

# ლოგისტიკური რეგრესიის მოდელი
მოცემულია დეითასეთი გულის შეტევის შესახებ და ლოგისტიკური რეგრესიის მოდელის მეშვეობით ხდება გულის შეტევის პროგნოზირება.
განხორციელდა შემდომი ეტაპები:
* დამოკიდებული და დამოუკიდბელი სვეტების განცალკევება
* სატრენინგოდ და სატესტოდა დაყოფა. სატესტოს ზომად აღებულია 30%
* მოვახდინეთ მონაცემთა სკალირება StandardScaler-ის გამოყენებით
* LogisticRegression მოდელის შემნა და სატრენინგო მონაცემებით დატრენინგება
* სატესტო მონაცემებზე შედეგის პროგნოზირება
  
მოდელის მიერ დაფიქსირებული ეფექტურობაა 0.8555555555555555 და ამ მოდელის მიხდევით დგინდება,
რომ 67.0, 0, 144, 0, 23, 0, 65000.0, 1.4, 139, 1, 0, 7 მახასიათებლების მქონდე პირი გადარჩება. 
მოცემული დეითასეტი შეგიძლიათ იხილოთ ბმულზე https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data

# გადაწყვეტილების ხის კლასიფიკაციის მოდელი
მოცემულია მანქანების შესახებ დათასეტი და გადაწყვეტილების ხის კლასიფიკაციის მოდელის გამოყენებით ხდება მანქანის მიერ მოხმარებული საწვავის პროგნოზირება.
განხორხიელდა რიგი ქმდებები null-ების შესავდებად:
* power სვეტში null-ების ამავე სვეტის მედიანით შევსება
* transmission სვეტში სიცარიელეების შევსება ყველაზე ხშირად გამეორებული მონაცემებით
* year სვეტის წაშლა, რაგდან ბევრი მონაცემი აკლია და Unnamed: 0 სვეტის წაშლა, რადგან არაფერში არ არის საჭირო
  
ამის შემდგომ მოხდა იმ სტრიქონების წაშლა, რომლებიც null-ებს შეიცავს.
რადგან უკვე ერთადერთი null-ის შემცველი სვეტი fuelType-ია, წაიშლება ის სტრიქონები, რომლებსაც დამოკიდებული ცვლადი არ აქვს განსაზღვრული

გვაქვს 3 კლასი: Diesel, Gasoline, Electro

შემდგმო განხორციელდა ქმედებები:
* შევქმენით LabelEncoder და კატეგორიული სვეტების რიცხვითში გადაყვანის მიზნით
* ხორციელდება დამოკიდებული და დამოუკიდებელი ცვლადების გაცალკევება
* ხდება მონაცემების სატრენინგოდ და სატესტოდ დაყოფა. სატესტოს ხომად აღებულია 30%
* ხორციელდება მონაცემთა სკალირება StandardScaler-ის გამოყენებით
* ხდება DecisionTreeClassifier მოდელის შექმნა და დატრენინგება
  
მოდელმა სატესტო მონაცემებზე აჩვენა ძალიან მაღალი ეფექტურობა 0.9913659068366827.
მოცემულმა მოდელბა გადაცემულ ახალ მონაცემზე აჩვენა, რომ ამ მახასიათებლების მქონე მანქანა იყენებს Gasoline-ს
დათასეტი შეგიძლიათ იხილოთ ბმულზე https://www.kaggle.com/datasets/fernandin83/carfueltype

# გამოყენებული ბიბლიოთეკები/თულები:
* pandas
* numpy
* matplotlib
* seaborn
* sklearn

# დამატებითი ინფორმაცია
ბაზის ფაილიები აღებულია www.kaggle.com პლატფორმიდან
