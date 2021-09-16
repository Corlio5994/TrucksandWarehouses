# TrucksProject
Repository for my Microsoft Learn IoT project! In this project I extend the functionality created over the MS Learn course by increasing the number of trucks and relocating to Australia.

# Concept
Initially, I wanted to create a new kind of device to represent warehouses which store products. Warehouses would also be responsible for maintaining the temperature of goods, but would have additional functionality to request supplies from other warehouses if they were running low on stock, or make a request to a remote supplier (which would bring a larger supply, but take longer). Each vehicle would start from a different warehouse. I think this would be a really valuable and interesting addition to the modelling project, but I quickly realised that the knowledge of the IoT pipeline and JavaScript, as well as the ability to quickly model computational problems, required to achieve something like this was beyond my personal abilities. 

Another interesting avenue to explore would involve setting up IoT Edge, so that large numbers of trucks could be connected to Edge and then sent to IoT Central, but I imagine this would take me even longer to investigate and implement than the other idea I had.

Instead, I thought it would be interesting to add some new visualisations, add a few extra trucks, and input new starting locations and destinations. To make the process of running the project easier, I also found out how to run multiple apps without requiring 6 separate command windows for each truck. This was, of course, much more manageable (especially considering that I started this project the day after it was due because the MS Learn course took longer than expected), and easier to achieve results, but I thought it was still a creative response. I hope you enjoy exploring the results I achieved! Unfortunately, I haven't been able to produce any graphics using PowerBI. I'm not entirely sure why, but it's interpreting all input data as location data, even though the separate telemetry inputs have different semantic types. I've been trying to fix this, but I don't have a solution, and even if I find one it's unlikely I'll be able to produce meaningful graphics before letting this project become 2 days overdue... 

# Setup 
Using 'npm run prepare' or 'npm install' will provide all required packages to run this project. Using 'npm run start' will bring all trucks live. Note that my personal Azure Maps and IoT Central keys are included in this project, but to completely recreate my process, you'd need to set up accounts with Azure Maps, IoT Central, EventHub, Blob Storage, StreamAnalytics and PowerBI. Another important consideration is that of issues with sending continuous streaming data- I noticed that my computer couldn't send data from all trucks simultaneously, so different vehicles would periodically appear disconnected in IoT Central. Depending on your personal system, you may experience similar issues if you were to run the same script, although this can be circumvented by only deploying some of the trucks (can be done manually).  