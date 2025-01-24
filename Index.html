import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.net.HttpURLConnection;
import java.net.URL;
import org.json.JSONObject;

public class WeatherApiClient {

    private static final String API_URL = "http://api.openweathermap.org/data/2.5/weather";
    private static final String API_KEY = "your_api_key_here"; // Replace with your API key

    public static void main(String[] args) {
        String city = "London"; // Example city
        fetchWeatherData(city);
    }

    public static void fetchWeatherData(String city) {
        try {
            // Construct the URL
            String urlString = String.format("%s?q=%s&appid=%s&units=metric", API_URL, city, API_KEY);
            URL url = new URL(urlString);

            // Open a connection
            HttpURLConnection connection = (HttpURLConnection) url.openConnection();
            connection.setRequestMethod("GET");

            // Read the response
            int responseCode = connection.getResponseCode();
            if (responseCode == HttpURLConnection.HTTP_OK) {
                BufferedReader in = new BufferedReader(new InputStreamReader(connection.getInputStream()));
                String inputLine;
                StringBuilder response = new StringBuilder();

                while ((inputLine = in.readLine()) != null) {
                    response.append(inputLine);
                }
                in.close();

                // Parse and display the JSON response
                parseAndDisplayWeatherData(response.toString());
            } else {
                System.out.println("Error: Unable to fetch data. HTTP response code: " + responseCode);
            }

        } catch (Exception e) {
            System.out.println("Error: " + e.getMessage());
        }
    }

    private static void parseAndDisplayWeatherData(String jsonResponse) {
        try {
            JSONObject jsonObject = new JSONObject(jsonResponse);

            // Extract weather information
            String cityName = jsonObject.getString("name");
            JSONObject main = jsonObject.getJSONObject("main");
            double temperature = main.getDouble("temp");
            int humidity = main.getInt("humidity");

            JSONObject weather = jsonObject.getJSONArray("weather").getJSONObject(0);
            String description = weather.getString("description");

            // Display the information
            System.out.println("Weather Data for " + cityName + ":");
            System.out.println("Temperature: " + temperature + " °C");
            System.out.println("Humidity: " + humidity + "%");
            System.out.println("Description: " + description);

        } catch (Exception e) {
            System.out.println("Error parsing JSON response: " + e.getMessage());
        }
    }
}
