## Case Study: Clean Architecture Project

Clean structured Flutter showcase project, using **`Bloc`**, **`GetIt`**, **`GoRouter`**, **`Hive`**, **`fpdart`**, **`freezed`**, secure **`JWT`** authentication, **`Crashlytics`**&**`Analytics`**, localization, custom theming and responsive UI.

<!-- ![](assets/readme/home_50fps_x425.gif) -->
<!-- MUST BE! : 50fps : x425 : Non Full HD (80%) -->
![](https://github.com/stdxpe/case_study_movies_project/raw/main/assets/readme/profile_50fps_x425.gif)
   
   
   
## Technical Highlights

- **`Architecture`** :  Project strictly follows `Clean Architecture` principles.

- **`State Management`** :  Implemented `Bloc` for complex UI state flows.

- **`Dependency Injection`** :  Registered all services and dependencies via `GetIt`

- **`Navigation`** :  Integrated `GoRouter` and automated auth-based `redirect` service.

- **`Monitoring`** :  Created centralized `Logger` with `Firebase Crashlytics`&`Analytics`

- **`Networking`** :  Implemented `Dio` as HTTP client with automated auth interceptors.

- **`Storage`** :  Implemented `Hive` to locally store and cache user preferences.

- **`Token Management`** :  Secured `JWT` tokens with encrypted `FlutterSecureStorage`

- **`Design`** :  Mapped pixel-perfect, adaptive/responsive `Figma` designs with `ScreenUtil`

- **`Animations`** :  Used `Lottie` and `flutter_animate` for smooth UI interactions.

- **`Theme`** :  Defined global component styles, typography, and `dark/light` color palettes.

- **`Error Handling`** :  Managed Domain-level failures with `fpdart` and `Either<L,R>`

- **`Type-Safety`** :  Used `freezed` to create immutable and type-safe Domain entities.
   
   
   
&nbsp;
<!-- ![](assets/readme/profile_50fps_x425.gif) -->
![](https://github.com/stdxpe/test/blob/main/poster.jpg)



## Project Structure
```bash
lib/
├── *core/
│   ├── constants/
│   ├── dependency_injection/
│   └── entities/
│   │   ├── failure/
│   │   ├── movie/
│   │   ├── paginated_movies/
│   │   ├── pagination/
│   │   ├── preferences/
│   │   ├── record/
│   │   ├── ui_side_effect/
│   │   └── user/
│   │
│   ├── errors/
│   └── extensions/
│   │
│   └── models/
│   │   ├── http_response/
│   │   ├── response_error_dto/
│   │   └── response_info_dto/
│   │
│   └── services/
│   │   ├── image_processing/
│   │   ├── locale/
│   │   ├── logger/
│   │   ├── navigation/
│   │   ├── network/
│   │   ├── secure_storage/
│   │   └── storage/
│   │
│   └── settings/
│   │   ├── settings_bloc/
│   │   └── global_event_dispatcher/
│   │
│   └── shared/
│   │   ├── components/
│   │   ├── overlays/
│   │   └── wrappers/
│   │
│   ├── theme/
│   └── utilities/
│
│   
├── *features/
│   ├── auth/
│   │   ├── data/
│   │   │   ├── datasources/
│   │   │   ├── models/
│   │   │   └── repositories/
│   │   │
│   │   └── domain/
│   │   │   ├── repositories/
│   │   │   └── usecases/
│   │   │
│   │   └── presentation/
│   │       ├── bloc/
│   │       ├── pages/
│   │       └── widgets/
│   │
│   └── home/
│   │   ├── data/
│   │   │   ├── datasources/
│   │   │   ├── models/
│   │   │   └── repositories/
│   │   │
│   │   └── domain/
│   │   │   ├── repositories/
│   │   │   └── usecases/
│   │   │
│   │   └── presentation/
│   │       ├── bloc/
│   │       ├── pages/
│   │       └── widgets/
│   │
│   └── profile/
│       ├── data/
│       │   ├── datasources/
│       │   ├── models/
│       │   └── repositories/
│       │
│       └── domain/
│       │   ├── entities/
│       │   ├── repositories/
│       │   └── usecases/
│       │
│       └── presentation/
│           ├── bloc/
│           ├── pages/
│           └── widgets/
│
└── *assets/
│   ├── fonts/
│   ├── icons/
│   ├── images/
│   ├── lottie/
│   └── translations/
│
├── .env.template
├── firebase_options.template
│
├── splash_page.dart
├── root_app.dart
└── main.dart

```
![](https://github.com/stdxpe/ecommerce_shopping_project/blob/dev/readme_doc/dark_mode.jpg)

  
  
&nbsp;
## Features & Development Notes

>Delivered all demanded features, including secure authentication, infinite scroll and pull-to-refresh on paginated home content, instant UI updates on favorite, user profile management, profile photo upload, bottom navigation with preserved page states, Lottie animations, custom theming, multi-language support, logger, and navigation/redirect service..
   
   
   
&nbsp;

    
![](https://github.com/stdxpe/case_study_movies_project/blob/main/assets/readme/validation_50fps_x425.gif)
```makefile
Authentication: (Demanded Requests)

- User login and registration functionality
- Secure storage of session token
- Automated redirections on successful login and auth-state changes
```

  
&nbsp;
  

![](https://github.com/stdxpe/case_study_movies_project/blob/main/assets/readme/home_50fps_x425.gif)
```makefile
Home Page: (Demanded Requests)

- Infinite scrolls and `pull-up-to-refresh` with loading indicator
- Pagination functionality using API-driven lists with lazy loading
- Instant UI updates on favorite movie toggles
```
  
  
&nbsp;

  
![](https://github.com/stdxpe/case_study_movies_project/raw/main/assets/readme/profile_50fps_x425.gif)
```makefile
Profile Page: (Demanded Requests)

- Displaying user information and profile details
- Displaying user's favorite movies list as lazy gridview
- Profile photo upload feature and ImageProcessingService
- Visually challenging LimitedOffersPage pixel-perfectly recreated from Figma design
```
  
  
&nbsp;

  
```makefile
Theme & Localization:

- Implemented custom themes, typography and dark/light color palettes
- Base attributes of all shared components defined in `ThemeData`
- Implemented `multi-language` support and runtime switching
- Settings and preferences stored locally and loaded instantly on startup
```
  
  
&nbsp;

  
```makefile
Navigation: (Demanded Requests)

- Navigation Service with `GoRouter`
- Redirects on startup and whenever auth-state changes
- Reacts to internet connectivity in real-time
- Page transitions using `BottomNavigationBar`
- Preserved HomePage state on tab switches
```
  
  
&nbsp;


![](https://github.com/stdxpe/test/blob/main/splash_and_icon.png)
```rust
Splash Screen and App Icon
```
  
  
&nbsp;

![](https://github.com/stdxpe/test/blob/main/crashlytics_and_logger.png)
```makefile
Logger Service:

- Implemented a centralized and class-aware custom LoggerService
- Provided helpers/extensions for global access without manual constructor injections
- Structured logs [LEVEL][ClassName][Message] formatting for consistent outputs
- Provided error, info, debug, warning, fatal LogLevel's, and custom Messages

📌 ’logger.f’, ’logger.w’ and ’logger.e’ sends reports to Crashlytics by default
```
  
  
&nbsp;

  
```yaml
It's all freezed:

All (Data) models/DTOs, (Domain) entities, Status unions, States, Events...
Created as immutable and type-safe `freezed` objects.
```
  
  
&nbsp;


```yaml
Everything's abstracted:

Worked with abstract classes throughout the entire project, to minimize dependencies.
All Core services, repositories, datasources, critical modules abstracted and DI-wired.
                  LocalStorageService ➙ LocalStorageServiceImpl (Hive)
                       NetworkService ➙ NetworkServiceImpl (Dio)  ...

📌 Even more;  Created `HttpResponse` ➙ instead of `DioResponse`
             `NetworkClientException` ➙ instead of `DioException`
```
  
  
&nbsp;
  
  
```makefile
Architecture:

Project document clearly states “Clean Architecture + MVVM + Bloc” requirements.
MVVM expectation interpreted as view–business separation, rather than `ChangeNotifier` usage.
Features were created Page-oriented, instead of being grouped by shared functionality.
Blocs acted as natural ViewModels, and since Clean Architecture inherently dictates
pages/ and bloc/ separation; the View–ViewModel pattern was achieved as a direct result.

Also, required expectations for Clean Architecture and dependency boundaries
were not explicitly defined on `Case Study Project Document`.
Therefore, applied strict Clean Architecture; followed best practices;
aimed to avoid anti-patterns; and focused on preventing any violations.
```
  
  
&nbsp;
  
  
```makefile
Error-Handling:

- Created custom Failure object, and folded on Bloc-level with (fpdart) Either<L,R>
- Data-level used try/catch's and throwed/rethrowed custom raw Exceptions
- Domain-level mapped/converted DataSource Exceptions to custom Failure types
- Therefore, Domain-level Failure object was not exposed to both Data-layer and UI

- UI displayed error messages gracefully with UISideEffect notifications
- Global errors handled with runZonedGuarded, FlutterError and PlatformDispatcher
```
```dart
📌 Note
/// We could’ve mapped [Exception]s to [Failure]s at `DataSource-level`..
/// and at `Repository-level`, without any try/catch, we could’ve written: 

         final result = await _remoteDataSource.getMovie();
         return result.fold(
            (failure) => Left(failure)
            (dto) => Right(dto.toEntity())

/// ..in a clean and elegant way. 

‼️ BUT, that would be an obvious `Clean Architecture` violation: 
///     - Because `Domain-layer` leaks into `Data-layer`
///     - and `Domain-entities` exposed to `Data-layer`


/// 📌 Industry-grade alternative:
/// [DataSource] returns `Either<DataFailure, DTO>` (uses `try/catch`)
/// [Repository] returns `Either<DomainFailure, Entity>` (uses `fold`)

/// Preferred the minimal pattern to avoid `over-engineering` for this case study project.
```
- Data-layer only used Data Models/DTOs, and Presentation-layer only used Domain Entities.
- So Data-layer never saw Domain Entities, and Presentation-layer never saw Data Models/DTOs.
  
  
&nbsp;
  
  
```makefile
Cross-Feature Dependencies:

- Features did NOT directly access other features.
- Any datasource, repository, usecase, or Bloc was never called from another feature.

Accessing/using domain repositories or usecases from different features, 
could make everything significantly easier, and reduce complexity..
‼️ BUT, under strict Clean Architecture rules, this is an anti-pattern and mostly forbidden.

Rather than being forced to define everything in a shared core repository,
Communication and notification signals between features, coordinated with `GlobalEventDispatcher`.
```
  
  
&nbsp;
  
  
```yaml
Bloc-Scopes & Lifecycle:

- Global Blocs (SettingsBloc and AuthBloc), defined as app-wide scoped.
- Page-scoped Blocs, created as factory, and disposed based on auth-state.

📌 All Blocs injected via DI, and provided on demand with `BlocWrapper`.
```
  
  
&nbsp;

# Project Flow
> [!NOTE]
> Following section demonstrates the project flow for `Movie`, `MoviesRemoteDataSource`, `MoviesRepository`, `Bloc`, `State`, `Event`, `HomePage` and `MoviesPageView`.
  

## Entity
`core/entities/movie.dart`
```dart
/// Immutable and type-safe Core-level Domain Entity for [Movie].
/// API-specific transformations and parsing handled at feature-level [MovieModel].

@freezed
sealed class Movie with _$Movie {
  const factory Movie({
    required String id,
    required String title,
    required String description,
    required String posterUrl,
    required String director,
    required bool isFavorite,
    required List<String> images,
    String? actors,
    String? awards,
    String? country,
    String? genre,
    String? writer,
    String? language,
    String? metascore,
    String? rated,
    String? released,
    String? runtime,
    String? year,
    String? imdbId,
    String? imdbRating,
    String? imdbVotes,
    String? type,
    bool? comingSoon,
  }) = _Movie;
}
```

&nbsp;
## Data Source
`features/home/data/datasources/movies_remote_data_source_impl.dart`
```dart
/// Concrete implementation of [MoviesRemoteDataSource].
/// Performs API requests, and response serialization/parsing with logs.

/// Functional error handling (fpdart, [Either], fold) is intentionally avoided here.
/// Throws custom raw [Exception]'s, instead of Domain-level [Failure] objects.

class MoviesRemoteDataSourceImpl implements MoviesRemoteDataSource {
  MoviesRemoteDataSourceImpl(this._client);

  final NetworkClient _client;

  @override
  Future<MoviesResponseDto> getPaginatedMovies({required int page}) async {
    const endpoint = ApiEndpoints.movies;
    final queryParameters = {'page': page};
    try {
      final response = await _client.get(endpoint, queryParameters: queryParameters);

      // UX Addition: NetworkClient already covers/overrides type check
      if (response.data is! Map<String, dynamic>) {
          logger.e(Messages.parsing.invalidFormat);
          throw ParsingException(Messages.parsing.invalidFormat);
      }

      final data = response.data as Map<String, dynamic>;
      final moviesResponseDto = MoviesResponseDto.fromJson(data);

      // Throws APIResponseException if internal response code is not valid
      moviesResponseDto.info.throwIfNotSuccess();

      logger.i(Messages.home.paginationSuccess(page: page));
      return moviesResponseDto;
    } catch (e) {
      logger.e(Messages.home.loadFailed(e.toString()));
      rethrow; // Rethrows NetworkClientException of NetworkClient
    }
  } ...
```
&nbsp;
## Repository
`features/home/data/repositories/movies_repository_impl.dart`
```dart
/// Concrete implementation of [MoviesRepository].

/// Converts Data-level models/DTOs to Domain-level entities with `.toEntity()` method.
/// Catches raw [Exception]'s from [MoviesRemoteDataSource] and converts/maps them into..
/// Domain-level [Failure] objects, by using [ExceptionMapper.mapToFailure] or just `toFailure(..)`.
/// Returns results as [Either]<[Failure], [Entity]> for functional error handling. // left(failure) or right(entity)

class MoviesRepositoryImpl implements MoviesRepository {
  MoviesRepositoryImpl(this._remoteDataSource);

  final MoviesRemoteDataSource _remoteDataSource;

  @override
  Future<Either<Failure, PaginatedMovies>> getPaginatedMovies({
    required int page,
  }) async {
    try {
      final dto = await _remoteDataSource.getPaginatedMovies(page: page);
      final paginatedMovies = dto.toEntity();

      logger.i(Messages.home.paginationSuccess(page: page));
      return right(paginatedMovies);
    } catch (e) {
      logger.e(Messages.home.paginationFailed(e.toString()));
      return left(e.toFailure());
    }
  } ...
```
&nbsp;
## Union Status
While `Failure` payload is a primitive String; `Success` payload is way more complex. Therefore, better to handle at `HomeState`.
   
`features/home/presentation/bloc/home_status.dart`
```dart
@freezed
sealed class HomeStatus with _$HomeStatus {
  const factory HomeStatus.initial() = _Initial;
  const factory HomeStatus.loading() = _Loading;
  const factory HomeStatus.success() = _Success;
  const factory HomeStatus.loadingMore() = LoadingMore;
  const factory HomeStatus.failure({String? message}) = _Failure;
}
```
&nbsp;
## State
`features/home/presentation/bloc/home_state.dart`
```dart
@freezed
sealed class HomeState with _$HomeState {
  const HomeState._();

  const factory HomeState({
    required HomeStatus status,
    required PaginatedMovies paginatedMovies,
    required int currentPageViewIndex,
    UISideEffect? uiSideEffect,
  }) = _HomeState;

  factory HomeState.initial() => HomeState(
    status: const HomeStatus.initial(),
    paginatedMovies: PaginatedMovies.initial(),
    currentPageViewIndex: 0,
  );

  List<Movie> get movies => paginatedMovies.movies;
  Movie get currentMovie => movies[currentPageViewIndex];
  Pagination get pagination => paginatedMovies.pagination;
}
```
&nbsp;
## Event
`features/home/presentation/bloc/home_event.dart`
```dart
@freezed
sealed class HomeEvent with _$HomeEvent {
  const factory HomeEvent.loadInitialMovies() = LoadInitialMovies;
  const factory HomeEvent.loadMoreMovies() = LoadMoreMovies;
  const factory HomeEvent.toggleFavoriteMovie(String movieId) = ToggleFavorite;
  const factory HomeEvent.changePageViewIndex(int index) = ChangePageViewIndex;
  const factory HomeEvent.scrollToTop() = ScrollToTop;
}
```
&nbsp;
## Bloc
`features/home/presentation/bloc/home_bloc.dart`
```dart
class HomeBloc extends Bloc<HomeEvent, HomeState> {
  final HomeUseCases _useCases;
  final GlobalEventDispatcher _eventDispatcher;
  StreamSubscription<SystemEvent>? _subscription;

  HomeBloc(this._useCases, this._eventDispatcher) : super(HomeState.initial()) {
    /// Simultaneous events are ignored by ’bloc_concurrency’
    on<LoadInitialMovies>(_onLoadInitialMovies);
    on<LoadMoreMovies>(_onLoadMoreMovies, transformer: droppable());
    on<ToggleFavorite>(_onToggleFavoriteMovie, transformer: droppable());
    on<ChangePageViewIndex>(_onChangePageViewIndex);
    on<ScrollToTop>(_onScrollToTop);

    add(const HomeEvent.loadInitialMovies());
  }

  Future<void> _onLoadInitialMovies(_, Emitter<HomeState> emit) async {
    emit(state.copyWith(status: const HomeStatus.loading()));

    final result = await _useCases.getPaginatedMovies(page: 1);

    result.fold(
      (failure) {
        logger.e(Messages.home.paginationFailed(failure.message));
        emit(state.copyWith(
            status: HomeStatus.failure(message: failure.message),
            uiSideEffect: UISideEffect.notifyError(failure.message)
        ));
      },

      (paginatedMovies) {
        logger.i(Messages.home.paginationSuccess(page: 1));
        emit(state.copyWith(
            status: const HomeStatus.success(),
            paginatedMovies: paginatedMovies,
            // Optional: UISideEffect.notifySuccess(..)
        ));
      },
    );
  }

  Future<void> _onLoadMoreMovies(_, Emitter<HomeState> emit) async {
    if (state.pagination.currentPage >= state.pagination.maxPage) return;
    // Optional: UISideEffect.notifyError(AppStrings.noMorePageToLoad);

    emit(state.copyWith(status: const HomeStatus.loadingMore()));
    await Future<void>.delayed(500.ms); // Shows LoadingMoreIndicator min 500.ms

    final nextPageToLoad = state.pagination.currentPage + 1;
    final result = await _useCases.getPaginatedMovies(page: nextPageToLoad);

    result.fold(
      (failure) {
        logger.e(Messages.home.paginationFailed(failure.message));
        emit(state.copyWith(
            status: HomeStatus.failure(message: failure.message),
            uiSideEffect: UISideEffect.notifyError(failure.message),
        ));
      },

      (response) {
        final updatedMovies = [...state.movies, ...response.movies];

        logger.i(Messages.home.paginationSuccess(page: nextPageToLoad));
        emit(state.copyWith(
            status: const HomeStatus.success(),
            paginatedMovies: response.copyWith(movies: updatedMovies),
            uiSideEffect: const UISideEffect.animateToNextPage(),
        ));
      },
    );
  }

  Future<void> _onToggleFavoriteMovie(
    ToggleFavorite event,
    Emitter<HomeState> emit,
  ) async {
    final result = await _useCases.toggleFavorite(movieId: event.movieId);

    result.fold(
      (failure) {
        logger.e(Messages.home.toggleFailed(event.movieId, failure.message));
        emit(state.copyWith(
            status: HomeStatus.failure(message: failure.message),
            uiSideEffect: UISideEffect.notifyError(failure.message),
        ));
      },

      (toggledMovie) {
        final newMovies = state.movies
            .map((movie) => (movie.id == toggledMovie.id) ? toggledMovie : movie)
            .toList(); // Replaces state with the toggled movie

        logger.i(Messages.home.favoriteToggled(event.movieId));
        emit(state.copyWith(
            status: const HomeStatus.success(),
            paginatedMovies: state.paginatedMovies.copyWith(movies: newMovies),
            uiSideEffect: UISideEffect.showFavoriteAnimation(
              state.currentMovie.isFavorite, // Shows lottie favorite overlay
        )));
        
        /// Broadcasts a global event to notify [FavoriteMoviesBloc]
        _eventDispatcher.publish(
          SystemEvent.movieFavoriteStatusChanged(movieId: toggledMovie.id),
        );
      },
    );
  }

  void _onChangePageViewIndex(
    ChangePageViewIndex event,
    Emitter<HomeState> emit,
  ) => emit(state.copyWith(currentPageViewIndex: event.index));

  void _onScrollToTop(_, Emitter<HomeState> emit) {
    /// Implemented inside Bloc, for ’Refresh’ functionality in future
    emit(state.copyWith(uiSideEffect: const UISideEffect.animateToTop()));
  }

  @override
  Future<void> close() {
    _subscription?.cancel();
    logger.d(Messages.core.disposed(getClassName));
    return super.close();
  }
}
```
&nbsp;
## UI: Page
`features/home/presentation/pages/home_page.dart`
```dart
class HomePage extends StatelessWidget {
  const HomePage({super.key});

  @override
  Widget build(BuildContext context) {
    return BlocWrapper<HomeBloc, HomeState>(
      provideMode: ProvideMode.factory,
      isLoading: (state) => state.status.whenOrNull(loading: () => true),
      isInitial: (state) => state.status.whenOrNull(initial: () => true),
      loadingOverlay: const LoadingOverlayAlternative(),
      uiSideEffects: (state) => state.uiSideEffect,
      noticationMode: NotificationMode.toast,

      listener: (context, state, bloc) {
        state.uiSideEffect?.whenOrNull(
          showFavoriteAnimation: (isFavorite) =>
              context.overlay.show(FavoriteOverlay(isFavorite: isFavorite)),
        );
      },

      builder: (context, state, bloc, isLoading) {
        return Scaffold(
          body: Stack(
            children: [
              MoviesPageview(),

              MovieInfoCard(movie: state.currentMovie),

              FavoriteButton(
                onTap: () => bloc.add(ToggleFavorite(state.currentMovie.id)),
                isFavorite: state.currentMovie.isFavorite,
              ),

              ScrollToTopButton(
                onTap: () => bloc.add(const ScrollToTop()),
                currentIndex: state.currentPageViewIndex,
              ),

              if (state.status is LoadingMore) LoadingMoreIndicator(),
            ],
          ).animate().fadeIn(),
        );
      },
    );
  }
}
```

&nbsp;
## UI: Widget
- Used `flutter_hooks` for PageController without StatefulWidget.
- Instead of passing state or data of the Bloc; `BlocWrapper` internally uses/reaches the same parent Bloc via `ProvideMode.subInstance`.

`features/home/presentation/widgets/movies_pageview.dart`  
```dart
class MoviesPageview extends HookWidget {
  const MoviesPageview({super.key});

  @override
  Widget build(BuildContext context) {
    final pageController = usePageController();

    return BlocWrapper<HomeBloc, HomeState>(
      provideMode: ProvideMode.subInstance,
      showLoadingOverlay: false,
      isLoading: (state) => state.status.whenOrNull(loading: () => true),
      noticationMode: NotificationMode.toast,

      listener: (context, state, bloc) {
        state.uiSideEffect?.whenOrNull(
          /// Automatically scrolls down after new movies fetched
          animateToNextPage: () async => pageController.nextPage(
            duration: 400.ms, curve: Curves.ease),

          /// Scrolls to top if HomeEvent.scrollToTop event emitted
          animateToTop: () async => pageController.animateToPage(
            0, duration: 400.ms, curve: Curves.easeInOut),
        );
      },

      builder: (context, state, bloc, isLoading) {
        return NotificationListener<OverscrollNotification>(
          /// Detects user overscrolls and emits LoadMoreMovies event,
          /// for ’Pull-up-to-load / Infinite Scrolling’ functionality
          onNotification: (notification) {
            if (notification.overscroll > AppConstants.sizes.maxOverscroll) {
              bloc.add(const LoadMoreMovies());
            }
            return true;
          },

          child: PageView.builder(
            controller: pageController,
            scrollDirection: Axis.vertical,
            physics: const ClampingScrollPhysics(),
            itemCount: state.movies.length,
            onPageChanged: (index) =>
                bloc.add(HomeEvent.changePageViewIndex(index)),
            itemBuilder: (context, index) =>
                MovieSwipeableCard(movie: state.movies[index]),
          ),
        );
      },
    );
  }
}
```

  
📌 High-level Flow:  `UI → Bloc → UseCases → Repository → DataSource`
  
- HomePage triggers HomeBloc event  
- HomeBloc calls HomeUseCases.getPaginatedMovies  
- UseCase calls MoviesRepository.getPaginatedMovies  
- Repository calls MoviesRemoteDataSource  
- DataSource fetches from API (via NetworkClient)  
- Response ➙ DTO ➙ toEntity() ➙ Either<Failure, Entity>  
- Bloc updates UI state  
- UI may show a loading overlay or a UISideEffect.
  
  
&nbsp;
## Installation
Highly recommended to clone this project to local machine for review:
```toml 
Quick run:  clone ➙ flutter pub get ➙ flutter run
```
Preferred a straightforward and effortless **`clone-and-run`** setup for reviewers.  
No action is required; codegen files and native docs included on GitHub repository.  
  
  
<details>
<summary>🔽🔽  <b>Further Setup Details</b>  🔽🔽</summary>

&nbsp;

```bash
git clone https://github.com/stdxpe/clean_architecture_case_study_project.git
```

```bash
cd clean_architecture_case_study_project
```

```bash
flutter pub get
```

📌 Optional:  Copy and fill templates. (See `firebase_options.template.dart` and `.env.template`)  
  
📌 Optional:  Execute for codegen files if necessary:  
```bash
dart run build_runner clean
dart run build_runner watch -d
```

```bash
flutter run
```

</details>
  
  
&nbsp;
## Final Note
Thanks to all hiring reviewers and engineering teams for evaluating this project.   
Feedbacks are highly appreciated, for guiding the project towards professional standards and hiring expectations.

&nbsp;
