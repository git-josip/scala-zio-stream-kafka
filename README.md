# scala-zio-stream-kafka

This project demonstrates the use of ZIO, ZIO Streams, and Kafka to process and analyze product reviews. The application reads JSONL files containing product reviews, processes them, and produces the results to Kafka topics.

## Features

- **ZIO**: Leverages ZIO for asynchronous and concurrent programming.
- **ZIO Streams**: Utilizes ZIO Streams for efficient file processing.
- **Kafka Integration**: Produces processed data to Kafka topics.
- **Error Handling**: Includes error handling and dead-letter queue for failed records.

## Prerequisites

- **Scala**: Ensure Scala is installed.
- **sbt**: The project uses sbt for build management.
- **Kafka**: A running Kafka instance is required.
- **Git LFS**: Used for managing large JSONL files.

## Setup

1. **Clone the repository**:
    ```sh
    git clone <repository-url>
    cd scala-zio-stream-kafka
    ```

2. **Install Git LFS**:
    ```sh
    git lfs install
    git lfs pull
    ```

3. **Install dependencies**:
    ```sh
    sbt update
    ```

## Configuration

- **Kafka**: Update the Kafka settings in `src/main/scala/com/reactive/streams/Main.scala` if necessary.

## Running the Application

1. **Start Kafka**: Ensure your Kafka instance is running.

2. **Run the application**:
    ```sh
    sbt run
    ```

## Project Structure

- `src/main/scala/com/reactive/streams/AverageMaxRating.scala`: Contains logic for processing product reviews and calculating top products.
- `src/main/scala/com/reactive/streams/Main.scala`: Contains logic for reading files, parsing reviews, and producing to Kafka.

## Usage

- **Processing Reviews**: The application reads reviews from a JSONL file, processes them, and produces results to Kafka.
- **Error Handling**: Failed records are sent to a dead-letter queue for further inspection.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgements

- **ZIO**: Asynchronous and concurrent programming library for Scala.
- **Kafka**: Distributed streaming platform.

## Contact

For any questions or issues, please open an issue in the repository.